# Reproducer

This reproducer demonstrates a bug in `react-native` where the codegen is not properly excluding libraries that are disabled in the `react-native.config.js` file.

## Steps to reproduce

1. Run `yarn install`
2. Run codegen or install pods `npx pod-install`
3. Check that codegen didn't exclude `react-native-screens` from: ios/build/generated/ios/RCTThirdPartyComponentsProvider.mm

## Expected behavior

The codegen should properly exclude the libraries that are disabled in the `react-native.config.js` file.
