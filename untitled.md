---
description: Jenkins包好apk後會把apk及測試檔丟到AWS Device Farm
---

# Jenkins update test to AWS Device Farm

## Install Plugins&Setting Jenkins

參考[https://docs.aws.amazon.com/zh\_tw/devicefarm/latest/developerguide/continuous-integration-jenkins-plugin.html](https://docs.aws.amazon.com/zh_tw/devicefarm/latest/developerguide/continuous-integration-jenkins-plugin.html)

## Setting Jenkins Project

進入Project Configure

### 拉到Post-build Actions，點選Add post-build action

![&#x65B0;&#x589E;AWS Device Farm](.gitbook/assets/screen-shot-2019-04-02-at-1.59.54-pm.png)

若專案目錄沒有做太多客製化設計的話，Application照以下設定就可以了

> \*\*/app/build/outputs/apk/release/app-release.apk

![&#x8A2D;&#x5B9A;&#x53C3;&#x8003;](.gitbook/assets/screen-shot-2019-04-02-at-2.04.10-pm.png)

記得把測試檔也放在專案專案目錄裡

> \*\*/test\_bundle.zip

![&#x8A2D;&#x5B9A;&#x53C3;&#x8003;](.gitbook/assets/screen-shot-2019-04-02-at-2.04.34-pm.png)

![&#x5176;&#x4ED6;&#x8A2D;&#x5B9A;](.gitbook/assets/screen-shot-2019-04-02-at-2.04.41-pm.png)

