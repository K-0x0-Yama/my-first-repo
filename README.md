# **IAM.7**

IAM.7の前提知識/関連知識

IAM.7の参考文献
[[IAM.7] IAM ユーザーのパスワードポリシーには強力な設定が必要です](https://docs.aws.amazon.com/ja_jp/securityhub/latest/userguide/securityhub-standards-fsbp-controls.html)


[クラスメソッド/AWSアカウントのパスワードポリシー](https://dev.classmethod.jp/articles/password_policy_for_aws_account/)
[AWS IAMのパスワードポリシーをAWS CLIから操作する](https://dev.classmethod.jp/articles/manage-iam-password-policy-via-cli/)

## IAM.7の概要
IAM ユーザーのパスワードポリシーには強力な設定が必要です

カテゴリ: 保護-セキュアなアクセス管理
緊急度: ミディアム
リソースタイプ: AWSアカウント
AWS Config ルール: iam-password-policy

パラメータ:
RequireUppercaseCharacters: true
RequireLowercaseCharacters: true
RequireSymbols: true
RequireNumbers: true
MinimumPasswordLength: 8


RequireUppercaseCharactersとは？
少なくとも 1 つの大文字が必要

RequireLowercaseCharactersとは？
少なくとも 1 つの小文字が必要

RequireSymbolsとは？
少なくとも 1 つの英数字以外の文字が必要
記号は「! @ # $ % ^ &amp; * ( ) _ + - = [ ] { } | '」の中から利用可能

RequireNumbersとは？
少なくとも 1 つの数字が必要

MinimumPasswordLengthとは？
パスワードの最小長
6から128まで指定可能

このコントロールは、IAM ユーザーのアカウントパスワードポリシーが次の推奨設定を使用しているかどうかを確認します。
RequireUppercaseCharacters: true
RequireLowercaseCharacters: true
RequireSymbols: true
RequireNumbers: true
MinimumPasswordLength: 8

Remediation
この問題を解決するには、推奨される構成を使用するようにパスワードポリシーを更新します。

パスワードポリシーを変更するには
IAM コンソール (https://console.aws.amazon.com/iam/) を開きます。
[Account settings (アカウント設定)] を選択します。
[Requires at least one uppercase letter (少なくとも 1 つの大文字が必要)] を選択します。
[Requires at least one lowercase letter (少なくとも 1 つの小文字が必要)] を選択します。
[Requires at least one non-alphanumeric character (少なくとも 1 つの英数字以外の文字が必要)] を選択します。
[Requires at least one number (少なくとも 1 つの番号が必要です)] を選択します。
[Minimum password length (パスワードの最小長)] に「8」と入力します。
