### STEP2-PASSWOED-MANAGER


## ステップ2

パスワードを保存し、出力するパスワードマネージャーをシェルスクリプトで作成します。パスワードの暗号化はしません。

以下の情報を保存・出力できるようにします。この情報はファイルに保存してください。

- サービス名
- ユーザー名
- パスワード

シェルスクリプトを実行すると、以下のメニューが表示されます。

```bash
パスワードマネージャーへようこそ！
次の選択肢から入力してください(Add Password/Get Password/Exit)：
```

Add Password が入力されると、サービス名、ユーザー名、パスワードの入力が求められ、入力された情報をファイルに保存します。
Get Password が入力されると、サービス名の入力が求められ、入力されたサービスのサービス名、ユーザー名、パスワードが表示されます。
Exit が入力されると、プログラムが終了します。
Exit が入力されるまではプログラムは終了せず、「次の選択肢から入力してください(Add Password/Get Password/Exit)：」が繰り返されます。

▼呼び出し

```bash
./password_manager.sh
```

▼アウトプット

```bash
パスワードマネージャーへようこそ！
次の選択肢から入力してください(Add Password/Get Password/Exit)：

# Add Password が入力された場合
サービス名を入力してください：
ユーザー名を入力してください：
パスワードを入力してください：

パスワードの追加は成功しました。
次の選択肢から入力してください(Add Password/Get Password/Exit)：

# Get Password が入力された場合
サービス名を入力してください：
## サービス名が保存されていなかった場合
そのサービスは登録されていません。
## サービス名が保存されていた場合
サービス名：hoge
ユーザー名：fuga
パスワード：piyo

次の選択肢から入力してください(Add Password/Get Password/Exit)：

# Exit が入力された場合
Thank you!
## プログラムが終了

# Add Password/Get Password/Exit 以外が入力された場合
入力が間違えています。Add Password/Get Password/Exit から入力してください。
```
