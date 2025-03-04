---
title: Power BI サービスでのコンテンツ共有方法の種類
date: 2021-09-30 00:00:00 
tags:
  - Power BI
  - Power BI サービス
  - Power BI Service
  - 共有
---


こんにちは、Power BI サポート チームの山崎です。 
Power BIのご利用を検討されているお客様からよくいただくご質問として、「レポートの共有方法が複数あり、どう共有するのがよいのかわからない」という課題があります。 

そこで、本ブログでは、Power BIにおけるレポートやダッシュボードのコンテンツの共有方法の詳細をご案内いたします。 
ご運用に沿った方法の検討において各方法について理解するためにお役に立てれば幸いです。 

<!-- more -->

> [!IMPORTANT]
> 本記事は弊社公式ドキュメントの公開情報を元に構成しておりますが、
> 本記事編集時点と実際の機能に相違がある場合がございます。
> 最新情報につきましては、参考情報として記載しておりますドキュメントをご確認ください。


---

## はじめに 

Power BIのご利用シナリオとして、Power BI Desktopで作成した .pbix ファイルや .pbit ファイルを他ユーザーへ直接渡すようなPower BIサービスを利用しないシナリオと、 

Power BI Desktopで作成した .pbix ファイルをPower BIサービスへ発行し、Power BI サービス上で共有を行うシナリオがございます。 
前者は一般的な .docx、 .pptx、.xlsxと同様に、ファイルとして他ユーザーに渡す方法となり、相手がPower BI Desktopを使用していれば可能となります。 

本ブログでは、後者のPower BIサービス上での共有におけるご案内となります。 

また、インターネット上のすべてのユーザーに公開するWebに公開機能は対象外となります。 

ご参考情報：
[Power BI Desktop とPower BI サービスの違い：Power BIでレポート作成・分析を行うために必要なものは？ | Japan CSS Support Power BI Blog (jpbap-sqlbi.github.io) ](https://jpbap-sqlbi.github.io/blog/powerbi/pbi_desktop_service/)
[Power BI から Web への公開 - Power BI | Microsoft Docs ](https://learn.microsoft.com/ja-jp/power-bi/collaborate-share/service-publish-to-web)


</br>

## 前提 

いずれの方法においても、以下どちらかの前提条件を満たしている必要があります。 

- 共有者、受信者の両者がPower BI ProまたはPPUライセンスユーザーである 
- コンテンツがPremium容量にあり、共有者がPower BI ProまたはPPUライセンスユーザーであり、受信者が  Power BI Free、Pro、PPUいずれかのライセンスユーザーである 

</br>

## Power BIサービス上でのコンテンツ共有方法の種類 

Power BIサービスでは、現在以下４つの方法でコンテンツを他者へ共有することが可能です。 

1. 直接アクセス 
2. リンク共有 
3. ワークスペースへのロール割り当て 
4. アプリ発行　 


各方法について以下にご説明いたします。 

</br>

### １．直接アクセス 

“Power BIでのコンテンツ共有“ において多くの方が最初に思い浮かぶ方法ではないかと思います。 
こちらは、従来から提供されている共有方法であり、対象のコンテンツ（レポートやダッシュボード）単位でユーザーやグループにアクセス権限を 
付与し共有する方法となります。編集権限は付与できませんが、アクセス権限付与時に、以下３つのオプションを選択することが可能です。 


- 受信者にこのレポートの共有を許可する 
- このレポートに関連づけられているデータでのコンテンツのビルドを受信者に許可する 
- メールの通知を送信 


<div align="center">
<img src="pic1.png" alt="画像1_直接アクセス" title="画像1_直接アクセス">
</div>


ご参考情報：
[同僚や他のユーザーと Power BI レポートやダッシュボードを共有する - Power BI | Microsoft Docs ](https://learn.microsoft.com/ja-jp/power-bi/collaborate-share/service-share-dashboards)

</br>

### ２．リンク共有（2021年9月時点ではレポートのみに使用可能）

2021年に追加された新機能であり、レポートへアクセスするためのリンクを作成し、そのリンクを共有する方法となります。
共有時には、リンクコピー以外に、OutlookやTeamsなど他サービスを介して共有することが可能です。
リンク共有には、３つの種類がございます。

- 組織内のユーザー
作成したリンクは、組織内のすべてのユーザーがアクセス可能となります。
このリンクは、外部ユーザーやゲスト ユーザーに対しては機能しません。
リンク作成時に、“設定”に記載の２つのオプションを選択可能です。

- 既存のアクセス許可を持つユーザー
作成したリンクは、直接アクセスにてすでにアクセス権限が付与されているユーザーまたはグループがアクセス可能となります。
オプションは、アクセス権限付与時に選択された設定に基づきます。（メール通知の送信オプションは対象外、リンクの送信で再度通知方法を選択します。）

- 特定のユーザー
作成したリンクは、既存のアクセス権を持たない特定のユーザーまたはグループがアクセス可能となります。
組織の Azure Active Directory (AAD) のゲストユーザーとは共有できますが、組織内のゲストではない外部ユーザーと共有することはできません。
リンク作成時に、“設定”に記載の２つのオプションを選択可能です。

<div align="center">
<img src="pic2.png" alt="画像2_リンク共有" title="画像2_リンク共有">
</div>


</br>

なお、各リンクの作成状況およびアクセスできるユーザー、グループについては、以下画面から確認・編集が可能です。

対象コンテンツの「アクセス許可の管理」＞　リンク　

<div align="center">
<img src="pic3.png" alt="画像3_リンクの管理" title="画像3_リンクの管理">
</div>


ご参考情報：
[Power BI レポートのリンクの共有 - Dynamics 365 Release Plan | Microsoft Docs](https://learn.microsoft.com/ja-jp/power-platform-release-plan/2021wave1/power-bi/sharing-links-power-bi-reports)
[Announcing the new sharing experience | Microsoft Power BI Blog | Microsoft Power BI](https://powerbi.microsoft.com/en-us/blog/announcing-the-new-sharing-experience/)

</br>

### ３．ワークスペースへのロール割り当て　

上記１，２のようにコンテンツごとの設定ではなく、ワークスペース単位でロールを付与する方法となります。
例えば、アクセス権限をもつフォルダ配下のすべてのファイルを開くことができるように、ワークスペースに対してユーザーまたはグループにビューアーのロールを
割り当てると、対象のユーザー（グループに所属するユーザー）はワークスペース内のすべてのコンテンツを閲覧できるようになります。
割り当て可能なロールは4種類あり、ロールによって許可されるワークスペース自体への権限や、コンテンツへの権限は異なりますので用途に応じて選択します。


<div align="center">
<img src="pic4.png" alt="画像4_ワークスペースへのロール割り当て" title="画像4_ワークスペースへのロール割り当て">
</div>



</br>

ロールの詳細につきましては、以下をご参考にしてください。

ご参考情報：
[Power BI の新しいワークスペースのロール - Power BI | Microsoft Docs](https://learn.microsoft.com/ja-jp/power-bi/collaborate-share/service-roles-new-workspaces#workspace-roles)

</br>

こちらは “新しいワークスペース” が対象になります。“クラッシックワークスペース” では使用できません。
ワークスペースの種類につきましては、以下をご参考にしてください。

ご参考情報：
[クラシックワークスペースと新しいワークスペースの違い：Power BIのワークスペースについて | Japan CSS Support Power BI Blog (jpbap-sqlbi.github.io)](https://jpbap-sqlbi.github.io/blog/powerbi/pbi_workspace_classic_and_app/)
[新しいワークスペースへのアクセス権をユーザーに付与する - Power BI | Microsoft Docs](https://learn.microsoft.com/ja-jp/power-bi/collaborate-share/service-give-access-new-workspaces)

</br>


### ４．アプリ発行　
ダッシュボードやレポートをパッケージ化しアプリとして作成し、組織全体、ユーザーまたはグループに対して発行した場合の共有方法となります。

アプリの詳細につきましては、以下をご参考にしてください。

ご参考情報：
[Power BI でアプリを発行する - Power BI | Microsoft Docs](https://learn.microsoft.com/ja-jp/power-bi/collaborate-share/service-create-distribute-apps)


アプリ発行時に、以下オプション設定が可能となります。
　
- すべてのユーザーが、ビルド アクセス許可を使用してアプリの基になるデータセットに接続することを許可します。
ユーザーがこのアプリ内のレポートのコピーを作成することを許可します。
- ユーザーが共有のアクセス許可を使用して、アプリとアプリの基になるデータセットを共有することを許可します。　


<div align="center">
<img src="pic5.png" alt="画像5_アプリ発行" title="画像5_アプリ発行">
</div>

</br>

上記でご案内した各方法を表におまとめしました。

| 共有の種類 | 対象 | 共有されたコンテンツへのアクセス方法 | 備考 |
| - | - | - | - |
| 直接アクセス | ・組織内のユーザー<br>・組織外のユーザー<br>・ゲストユーザー | ”自分と共有”からアクセスします。 | ・従来の共有方法<br>・組織内外のユーザーに対して共有が可能<br>・レポート、ダッシュボードに使用可能 |
| リンクの共有 | ※リンクの種類によって異なります。<br>◆組織内のユーザー<br>・組織内のユーザー<br><br>◆既存のアクセス許可を持つユーザー<br>・組織内のユーザー<br>・ゲストユーザー<br>・組織外のユーザー<br><br>◆特定のユーザー<br>・組織内のユーザー<br>・ゲストユーザー | 共有されたリンクからアクセスします。 | ・レポートのみに使用可能（2021年9月現在）<br>・各対象にわけてリンクを作成でき、そのリンクをOutlookやTeamsを介して共有することが可能 |
| ワークスペースへのロール割り当て | ・組織内のユーザー<br>・ゲストユーザー | 対象のワークスペースにアクセスします。 | ・ワークスペース単位で管理が可能<br>・編集権限を付与することが可能 |
| アプリ発行 | ・組織内のユーザー<br>・ゲストユーザー<br>・組織外のユーザー | 対象のアプリにアクセスします。 | ワークスペース内に含まれるレポート、ダッシュボードからアプリに含めるコンテンツを選択し、アプリ単位で共有が可能 |
|  |

</br>

以上、本ブログが少しでも皆様のお役に立てますと幸いでございます。

---

**アンケートご協力のお願い**
Japan CSS Support Power BI Blog では、作成する記事やブログの品質向上を目的に、匿名回答でのアンケートを実施しております。
ユーザー様のご意見・ご要望を参考に今後もお役に立てるブログを目指してまいりますので、ぜひご協力いただけますと幸いでございます。 

※　所要時間は1分程度となります。
[【ご協力のお願い】Microsoft Japan CSS Power BI Blog ご利用に関するアンケート](https://jpbap-sqlbi.github.io/blog/powerbi/pbi_blogsurvey2022/)