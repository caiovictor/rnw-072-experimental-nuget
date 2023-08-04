# rnw-072-experimental-nuget

Testing experimental nuget in an RNW csharp app with a dependency on an RNW csharp library.

MyApp has created by commands

```
npx react-native init MyApp --version "latest"
cd MyApp
npx react-native-windows-init --overwrite --language "cs" --projectType "app" --experimentalNuGetDependency true
```

react-native-native-module-c-sharp has created follow [official documentation](https://microsoft.github.io/react-native-windows/docs/native-modules-setup#creating-a-new-native-module-library-project)

```
npx create-react-native-module NativeModuleCSharp
cd react-native-native-module-c-sharp
yarn install
npx react-native-windows-init --version latest --projectType lib --language cs --overwrite --experimentalNuGetDependency true
```

After creating the packages, myLibrary was added as a myApp dependency:

```
cd MyApp
yarn add file:../react-native-native-module-c-sharp
```

Finishing did autolink:

```
npx react-native autolink-windows
```

Using:

- Yarn v1.21.1
- Node v16.13.1
- Windows Powershel v5.1.19041.3031
