【記錄】學習 React Native ＆ 遇到的狀況
======================================
以下記錄皆以 iOS 為主！

## 相關網站

[React Native 官網](https://facebook.github.io/react-native)

[React Native GitHub](https://github.com/facebook/react-native)

[React 官網](https://reactjs.org/)

## 安裝
開發平台：macOS、目標平台：iOS

建置專案前，必須先安裝：
* [Homebrew](http://brew.sh/)
* Node
```bash
brew install node
```
* [Watchman](https://facebook.github.io/watchman)
```bash
brew install watchman
```
* React Native CLI
```bash
npm install -g react-native-cli
```
* [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12)

## 建立＆執行專案
建立名稱為「AwesomeProject」的專案
```bash
react-native init AwesomeProject
```

進入「AwesomeProject」專案資料夾
```bash
cd AwesomeProject
```

使用 iOS 模擬器啟動專案
```bash
react-native run-ios
```
<a><img src="https://facebook.github.io/react-native/img/iOSSuccess.png" title="source: imgur.com" width="250" height="400" /></a>
