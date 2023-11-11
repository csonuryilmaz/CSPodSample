# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

target 'Pod-sample-app' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!
	pod 'CS_iOS_SDK'

end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    if target.respond_to?(:product_type) and target.product_type == "com.apple.product-type.bundle"
      target.build_configurations.each do |config|
        config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '13.0'
      end
    end
  end
end
