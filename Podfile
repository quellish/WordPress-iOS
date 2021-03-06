source 'https://github.com/CocoaPods/Specs.git'

inhibit_all_warnings!
use_frameworks!

platform :ios, '10.0'
workspace 'WordPress.xcworkspace'



## Pods shared between all the targets
## ===================================
##
def shared_with_all_pods
    pod 'WordPressShared', '~> 1.0.6'
    pod 'CocoaLumberjack', '3.4.2'
    pod 'FormatterKit/TimeIntervalFormatter', '1.8.2'
    pod 'NSObject-SafeExpectations', '0.0.3'
    pod 'UIDeviceIdentifier', '~> 0.4'
end

def shared_with_networking_pods
    pod 'AFNetworking', '3.2.1'
    pod 'Alamofire', '4.7.2'
    pod 'wpxmlrpc', '0.8.3'
    pod 'WordPressKit', '1.1'
end

def shared_test_pods
    pod 'OHHTTPStubs', '6.1.0'
    pod 'OHHTTPStubs/Swift', '6.1.0'
    pod 'OCMock', '~> 3.4'
end



## WordPress iOS
## =============
##
target 'WordPress' do
    project 'WordPress/WordPress.xcodeproj'

    shared_with_all_pods
    shared_with_networking_pods

    ## Third party libraries
    ## =====================
    ##
    pod '1PasswordExtension', '1.8.5'
    pod 'HockeySDK', '5.1.2', :configurations => ['Release-Internal', 'Release-Alpha']
    pod 'MRProgress', '0.8.3'
    pod 'Reachability',    '3.2'
    pod 'SVProgressHUD', '2.2.5'
    pod 'Crashlytics', '3.10.1'
    pod 'BuddyBuildSDK', '1.0.17', :configurations => ['Release-Alpha']
    pod 'Gifu', '3.0.0'
    pod 'MGSwipeTableCell', '1.6.7'
    pod 'lottie-ios', '2.5.0'
    pod 'Starscream', '3.0.4'
    pod 'ZendeskSDK', '1.11.2.1'


    ## Automattic libraries
    ## ====================
    ##
    pod 'Automattic-Tracks-iOS', :git => 'https://github.com/Automattic/Automattic-Tracks-iOS.git', :tag => '0.2.3'
    pod 'Gridicons', '0.15'
    pod 'NSURL+IDN', '0.3'
    pod 'WPMediaPicker', :git => 'https://github.com/wordpress-mobile/MediaPicker-iOS.git', :commit => 'b5ae03494596e3da7a8f814f9cab8e96ca345bc8'
    pod 'WordPressAuthenticator', :git => 'https://github.com/wordpress-mobile/WordPressAuthenticator-iOS.git', :commit => 'd0b3c02'
    pod 'WordPress-Aztec-iOS', :git => 'https://github.com/wordpress-mobile/AztecEditor-iOS.git', :commit =>'c38d29b09cc9710ef307891f76a02c80a7002a59'
    pod 'WordPress-Aztec-iOS/WordPressEditor', :git => 'https://github.com/wordpress-mobile/AztecEditor-iOS.git', :commit => 'c38d29b09cc9710ef307891f76a02c80a7002a59'
    pod 'WordPressUI', '1.0.4'

    target 'WordPressTest' do
        inherit! :search_paths

        shared_test_pods
        pod 'Nimble', '~> 7.1.1'
    end


    ## Share Extension
    ## ===============
    ##
    target 'WordPressShareExtension' do
        inherit! :search_paths

        shared_with_all_pods
        shared_with_networking_pods

        pod 'WordPress-Aztec-iOS', :git => 'https://github.com/wordpress-mobile/AztecEditor-iOS.git', :commit =>'c38d29b09cc9710ef307891f76a02c80a7002a59'
        pod 'WordPress-Aztec-iOS/WordPressEditor', :git => 'https://github.com/wordpress-mobile/AztecEditor-iOS.git', :commit => 'c38d29b09cc9710ef307891f76a02c80a7002a59'
        pod 'WordPressUI', '1.0.4'
        pod 'Gridicons', '0.15'
    end


    ## DraftAction Extension
    ## =====================
    ##
    target 'WordPressDraftActionExtension' do
        inherit! :search_paths

        shared_with_all_pods
        shared_with_networking_pods

        pod 'WordPress-Aztec-iOS', :git => 'https://github.com/wordpress-mobile/AztecEditor-iOS.git', :commit =>'c38d29b09cc9710ef307891f76a02c80a7002a59'
        pod 'WordPress-Aztec-iOS/WordPressEditor', :git => 'https://github.com/wordpress-mobile/AztecEditor-iOS.git', :commit => 'c38d29b09cc9710ef307891f76a02c80a7002a59'
        pod 'WordPressUI', '1.0.4'
        pod 'Gridicons', '0.15'
    end


    ## Today Widget
    ## ============
    ##
    target 'WordPressTodayWidget' do
        inherit! :search_paths

        shared_with_all_pods
        shared_with_networking_pods
    end
end



## WordPress.com Stats
## ===================
##
target 'WordPressComStatsiOS' do
    project 'WordPressComStatsiOS/WordPressComStatsiOS.xcodeproj'

    shared_with_all_pods
    shared_with_networking_pods

    ## Automattic libraries
    ## ====================
    ##
    pod 'WordPressUI', '1.0.4'

    target 'WordPressComStatsiOSTests' do
        inherit! :search_paths

        shared_test_pods
    end
end
