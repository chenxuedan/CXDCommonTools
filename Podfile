# Uncomment the next line to define a global platform for your project
source 'https://github.com/CocoaPods/Specs.git'

platform :ios, '9.0'

inhibit_all_warnings!

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      if config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'].to_f < 8.0
        config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '8.0'
      end
    end
  end
end

target 'CXDCommonTools' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!

  pod 'SDWebImage'
  pod 'Masonry'
  
  # Pods for CXDCommonTools

  target 'CXDCommonToolsTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'CXDCommonToolsUITests' do
    # Pods for testing
  end

end
