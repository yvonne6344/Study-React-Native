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


## 使用第三方套件
舉例：使用 [victory-native](https://github.com/FormidableLabs/victory-native) 這個圖表套件。(相關網站是 [victory](http://formidable.com/open-source/victory)，為 React 圖表套件。)

### 如何使用？
* 安裝 victory-native
  ```bash
  $ npm install victory-native --save
  ```
* 安裝 react-native-svg
  ```bash
  $ npm install react-native-svg --save
  ```
* 最好再 npm install 一次
  ```bash
  $ npm install
  ```
* 連結 react-native-svg
  ```bash
  $ react-native link react-native-svg
  ```
  <a><img src="https://i.imgur.com/QDe6nZj.png" title="source: imgur.com" width="700" height="130" /></a>

* 執行後，報錯：No component found for view with name "RNSVGPath"。

  <a><img src="https://i.imgur.com/RrlqJz6.png" title="source: imgur.com" width="250" height="500" /></a>

  解法：至 ios 資料夾，開啟專案，手動加入資源庫 libRNSVG.a (房屋）＆ 刪除 libRNSVG.a、libRNSVG-tvOS.a（柱狀）

  <a><img src="https://i.imgur.com/ruI31Id.png" title="source: imgur.com" width="300" height="150" /></a>

  <a><img src="https://i.imgur.com/LiVbnAN.png" title="source: imgur.com" /></a>
  
  <a><img src="https://i.imgur.com/yVfSUY2.png" title="source: imgur.com" /></a>


## 注意可能會遇到的坑

【情況一】設備太差

注意：因為啟動模擬器很耗效能，當電腦記憶體不足，可能會失敗當掉，必須重啟！

【情況二】終端機 Run 完，但 iOS 模擬器未成功啟動（正常情況會自動跳出模擬器視窗）

解法：砍掉 build 資料夾，再重新啟動一次（當模擬器啟動失敗時，可以用這招試試）
  
<a><img src="https://i.imgur.com/jFHYuoe.png" title="source: imgur.com" width="350" height="150" /></a>

【情況三】指終端機尚未執行完，模擬器卻已開始執行。只要等終端機跑完，模擬器再重 Run 就可以了 (command+R)。

<a><img src="https://i.imgur.com/P5GBcLf.png" title="source: imgur.com" width="350" height="150"/></a>
