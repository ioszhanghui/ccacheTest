# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

post_install do |installer_representation|
    installer_representation.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            #关闭 Enable Modules
            config.build_settings['CLANG_ENABLE_MODULES'] = 'NO'
            
            # 在生成的 Pods 项目文件中加入 CC 参数，路径的值根据你自己的项目来修改
            config.build_settings['CC'] = '$(PODS_ROOT)/ccache-clang'
        end
    end
end


target 'ccacheTest' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!
pod 'MLeaksFinder'
pod 'Masonry'
pod 'YYCategories'
pod 'AFNetworking'
pod 'SDWebImage'

  # Pods for ccacheTest

  target 'ccacheTestTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'ccacheTestUITests' do
    # Pods for testing
  end

end
