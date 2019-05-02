# Jenkins assemble apk

```
docker run -d -p 8080:8080 -p 50000:50000 --name MyJenkins \
-v [Home Directory]/jenkins_home:/var/jenkins_home a9911131/jenkins-android
```

## Build Jenkins

輸入以下指令下載Jenkins，並且啟動：

```text
$ docker run -d -p 8080:8080 -p 50000:50000 --name MyJenkins \
-v [Home Directory]/jenkins_home:/var/jenkins_home a9911131/jenkins-android
```

啟動後，就可以使用瀏覽器訪問[http://localhost:8080](http://localhost:8080)

## Create New Jobs

### Click New Item

click **New Item** on left menu, then ...

![&#x8F38;&#x5165;&#x4EFB;&#x52D9;&#x540D;&#x7A31;&#xFF0C;&#x9EDE;&#x9078;Freestyle project&#xFF0C;&#x7136;&#x5F8C;&#x9032;&#x5165;&#x4E0B;&#x4E00;&#x6B65;&#x9A5F;](.gitbook/assets/assets_-lzee0kum2_3n5nbzc5j_-lzegwyosp8nhcoeyxcs_-lzei0ghjzmb1xuvmyie_screen-shot-2019-02-21-at-17.0.png)

進入設定頁

### Source Code Management

選取Git，並且設定Repository URL及Credentials

### Build

![&#x65B0;&#x589E;Invoke Gradle script](.gitbook/assets/screen-shot-2019-03-06-at-2.27.24-pm.png)

#### Assemble signed apk

```text
clean
assembleRelease
-Pandroid.injected.signing.store.file=[keystore_path]
-Pandroid.injected.signing.store.password=[store_password]
-Pandroid.injected.signing.key.alias=[key_alias]
-Pandroid.injected.signing.key.password=[key_password]
```

Save

