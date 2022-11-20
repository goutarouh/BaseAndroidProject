# BaseAndroidProject

Androidアプリ開発のためのベースプロジェクト

## Usage

1. `settings.gradle`の修正
```
rootProject.name = "変更後の名前"
```

2. `app:build.gradle.kts`の修正
```
namespace = "変更後のパッケージ"
applicationId = "変更後のパッケージ"
```

3. `:data build.gradle.kts`の修正
```
namespace = "変更後のパッケージ.data"
```

4. ソースコードのパッケージ名修正
- `com.github.goutarouh.baseandroidproject`を右クリック
  - `Refactor` -> `Rename` -> `In Whole Project` と画面の指示に従い、最後に新たなパッケージ名を入力する

5. アプリ名変更 (`strings.xml`)
```
<resources>
   <string name="app_name">アプリ名</string>
</resources>
```

6. InstrumentedTestの修正
```
assertEquals("変更後のパッケージ", appcContext.packageName)
```

7. テーマ名の修正
- AndroidManifestの `android:theme`で右クリック
  - `Refactor` -> `Rename` で変更するテーマ名を入力

8. アプリケーションクラス名を変更
- `BaseAndroidApplication`を右クリック
  - `Refactor` -> `Rename` で変更

## Author

[twitter](https://twitter.com/gotlinan)
