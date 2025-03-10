# 概要

## GitHubを利用するメリット

Vivliostyle Pubはユーザーファイルの管理に、外部のバージョン管理システム、[GitHub](https://github.co.jp/)を利用しています。ユーザにとってバージョン管理システムは、以下のようなメリットがあります。

1. ファイルの変更履歴が記録できる
2. ファイルを以前の状態に戻せる
3. 複数ユーザによる共同編集ができる

残念ながら、現在のバージョンで上記、1、2はVivliostyle Pub上から実行できません。これらの機能は各種GitHubクライアントでご利用ください。[“Sourcetree”](https://www.sourcetreeapp.com/) など無料で使えるクライアントが各種あります。たとえば、GitHubの公式クライアントである[GitHub Desktop](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop)（無料）での操作は、下記を参照してください。

- [Viewing the branch history](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/viewing-the-branch-history)
- [Committing and reviewing changes to your project](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/committing-and-reviewing-changes-to-your-project)

ここでは上記3、複数ユーザによる共同編集を、Vivliostyle Pubでおこなう方法について説明します。

## 共同編集の概要

（この文書では、個々の作業者を「コミッター」、プロジェクトを統括する者を「管理者」とよびます）

共同編集では、GitHubの[“protected branches”](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches)機能を使います。この機能により、本流であるデフォルトブランチで直接編集することが禁止され、作業者は傍流である自分の作業ブランチで編集し、これを管理者のレビューを介してデフォルトブランチへ合流させることが徹底されます。こうした共同作業の結果、間違いの少ない文書を効率的に制作できます。

共同編集は、おおむね以下のような手順ですすめます（次節以降で説明します）。

1. [コミッターがGitHubのリポジトリでブランチを新規作成する](/multi-user-collaborative-editing/working-procedure-first-part.md#コミッターがgithubのリポジトリでブランチを新規作成)
1. [コミッターがVivliostyle Pubでそのブランチを選択する](/multi-user-collaborative-editing/working-procedure-first-part.md#コミッターがvivliostyle-pubでブランチを選択)
1. [コミッターがVivliostyle Pubで文書を編集し、保存する](/multi-user-collaborative-editing/working-procedure-first-part.md#コミッターがvivliostyle-pubで文書を編集／保存)
1. [コミッターがGitHubでプルリクエストを作成する](/multi-user-collaborative-editing/working-procedure-latter-part.md#コミッターがgithubでプルリクエストを作成)
1. [ 管理者がGitHubでプルリクエストをレビューし、承認とマージをする](/multi-user-collaborative-editing/working-procedure-latter-part.md#%E7%AE%A1%E7%90%86%E8%80%85%E3%81%8Cgithub%E3%81%A7%E3%83%97%E3%83%AB%E3%83%AA%E3%82%AF%E3%82%A8%E3%82%B9%E3%83%88%E3%82%92%E3%83%AC%E3%83%93%E3%83%A5%E3%83%BC%E3%80%81%E6%89%BF%E8%AA%8D%E3%80%81%E3%83%9E%E3%83%BC%E3%82%B8)

## 共同編集に必要な条件

上に述べた[“protected branches”](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches)機能を自分のリポジトリで使うには、GitHubの有償アカウントを取得するか、無償アカウント（Free）の場合はリポジトリを公開（Public）する必要があります。詳細は下記を参照してください。

- [GitHub の商品と価格プランの概要](https://docs.github.com/en/get-started/learning-about-github/githubs-products)

ただし、無償アカウントであっても、有資格者からリポジトリに招待されれば共同編集に参加できます。以下を参考にして下さい。

- **参考：**[Inviting collaborators to a personal repository](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-user-account/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository)