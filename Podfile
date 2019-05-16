using_local_pods = false

platform :ios, '11.3'

# ignore all warnings from all pods
inhibit_all_warnings!

if using_local_pods
  # Pull pods from sibling directories if using local pods
  target 'EosioSwiftVaultSignatureProvider' do
    use_frameworks!

    pod 'EosioSwift', :path => '../eosio-swift'
    pod 'EosioSwiftEcc', :path => '../eosio-swift-ecc'
    pod 'EosioSwiftVault', :path => '../eosio-swift-vault'
    pod 'SwiftLint'

    target 'EosioSwiftVaultSignatureProviderTests' do
      inherit! :search_paths
      pod 'EosioSwift', :path => '../eosio-swift'
      pod 'EosioSwiftEcc', :path => '../eosio-swift-ecc'
      pod 'EosioSwiftVault', :path => '../eosio-swift-vault'
    end
  end
else
  # Pull pods from sources above if not using local pods
  target 'EosioSwiftVaultSignatureProvider' do
    use_frameworks!

    pod 'EosioSwift', '~> 0.1.0'
    pod 'EosioSwiftEcc', '~> 0.1.0'
    pod 'EosioSwiftVault', '~> 0.1.0'
    pod 'SwiftLint'

    target 'EosioSwiftVaultSignatureProviderTests' do
      inherit! :search_paths
      pod 'EosioSwift', '~> 0.1.0'
      pod 'EosioSwiftEcc', '~> 0.1.0'
      pod 'EosioSwiftVault', '~> 0.1.0'
    end
  end
end
