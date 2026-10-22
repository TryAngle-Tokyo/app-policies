# app-policies

株式会社TRYANGLEのアプリ別プライバシーポリシーを公開するための共通リポジトリです。
今後のプロジェクトも、アプリ専用フォルダを追加して利用できます。
ゲーム本体のリポジトリとは分けて、公開用の静的ページを管理します。

## 公開中のページ

| アプリ | 掲載用HTML | 公開URL |
| --- | --- | --- |
| ピタッと！ひらがな | [pitattohiragana/index.html](./pitattohiragana/index.html) | [プライバシーポリシー](https://tryangle-tokyo.github.io/app-policies/pitattohiragana/) |
| ピタッと！カタカナ | [pitattokatakana/index.html](./pitattokatakana/index.html) | [プライバシーポリシー](https://tryangle-tokyo.github.io/app-policies/pitattokatakana/) |

## 追加準備中のページ

| アプリ | 掲載用HTML | 公開予定URL |
| --- | --- | --- |
| BubbleZero | [bubblezero/index.html](./bubblezero/index.html) | [プライバシーポリシー](https://tryangle-tokyo.github.io/app-policies/bubblezero/) |
| カードのおかたづけ（CardSorting） | [cardsorting/index.html](./cardsorting/index.html) | [プライバシーポリシー](https://tryangle-tokyo.github.io/app-policies/cardsorting/) |

BubbleZeroは公開元へpush済みです。CardSortingも公開元への反映後、公開URLの閲覧を確認します。

この一覧は公開ページの案内です。各アプリのストア審査・配布状況を示すものではありません。

## ファイル構成と公開方法

```text
app-policies/
├── .nojekyll
├── README.md
├── pitattohiragana/
│   └── index.html
├── pitattokatakana/
│   └── index.html
├── bubblezero/
│   └── index.html
└── cardsorting/
    └── index.html
```

公開元は `gh-pages` ブランチのルートです。
GitHub Pagesが静的ファイルを配信し、各アプリのURLは次の形式になります。

```text
https://tryangle-tokyo.github.io/app-policies/<アプリ専用フォルダ>/
```

`.nojekyll` はJekyllによる変換を無効にするためのファイルです。

GitHub上では `gh-pages` → アプリ専用フォルダ → `index.html` の順に開くと、HTMLを確認できます。
実際の表示は上表の公開URLから確認します。公開設定は、設定を確認できる権限のあるアカウントで **Settings → Pages** を開きます。

## 新しいアプリを追加する

1. 他のアプリと重複しない、英小文字・数字・ハイフンを基本とするフォルダ名を決めます。公開後はURLの一部になるため、継続利用できる名前にします。
2. `<アプリ専用フォルダ>/index.html` を作成します。既存ページは構成の参考にできますが、本文はそのアプリの実装・SDK・広告設定・保存方式に合わせます。
3. アプリ名、必要なアプリ識別情報、運営者、問い合わせ先、データの収集・利用・共有、安全な取扱い、保持・削除、最終更新日を確認します。対象ユーザーに応じた説明も用意します。
4. 対象プロジェクトの承認・レビュー手順に従って公開し、このREADMEの一覧にも追加します。
5. GitHub Pagesの反映後、ログインなしでHTTPS閲覧できること、スマートフォン表示、本文とリンクを確認します。
6. 確認した公開URLをアプリ内のリンクとストア管理画面に設定し、実際のアプリからも遷移を確認します。

## 本文の更新と製品版への移行

公開ページを更新するときは、該当アプリの `index.html` と最終更新日を更新します。
各プロジェクトに管理用の本文コピーがある場合は、同じ内容に同期し、どの版を公開したか追跡できるようにします。

同じURLを維持する場合、ポリシー本文の更新のためにアプリ内リンクを変更する必要はありません。
テスト広告から本番広告へ切り替える場合やSDK・収集データ・利用目的等を変える場合は、製品版の審査提出前に本文を実際の設定と照合します。
Google PlayのData Safety等の申告内容が変わる場合は、それらも更新します。ページの更新だけでリリース条件がすべて成立するわけではありません。

フォルダ名の変更やページの削除は、配布済みアプリやストアのリンク切れにつながります。
既存URLを使う利用者への影響を確認してから行います。

## 公開範囲と安全面

このリポジトリのファイルとGit履歴は公開されます。
公開用本文と案内だけを置き、ゲームの非公開ソース、社内資料、鍵、認証情報、個人情報、内部の検証ログは含めません。

一般の閲覧者は、書き込み権限なしに元ファイルや配信内容を変更できません。
第三者によるforkや変更提案も、それだけでは公開元へ反映されません。
書き込み・管理権限は必要な担当者に限定し、管理アカウントの多要素認証などで保護します。
これは管理上の注意点であり、現在の全アカウント・権限設定を監査済みとするものではありません。

公開ページはHTTPSで配信し、静的な本文とリンクを基本にします。
フォーム、アクセス解析、広告、外部スクリプト等を追加する場合は、ページ閲覧時のデータの取扱いも再確認します。
GitHub Pages側でのログの取扱いは、各ポリシーの「このページの閲覧について」で説明します。

## 参考

- [Google Play：ユーザーデータとプライバシーポリシーの要件](https://support.google.com/googleplay/android-developer/answer/10144311?hl=ja)
- [GitHub Pagesの利用制限](https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits)
- [GitHub PagesのHTTPS設定](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https)

GitHub Pagesを他の用途へ広げる場合は、商取引や商用SaaS等に関する利用制限も確認してください。
