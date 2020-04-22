# <a name="how-to-run-the-completed-project"></a><span data-ttu-id="431ee-101">完了したプロジェクトを実行する方法</span><span class="sxs-lookup"><span data-stu-id="431ee-101">How to run the completed project</span></span>

## <a name="prerequisites"></a><span data-ttu-id="431ee-102">前提条件</span><span class="sxs-lookup"><span data-stu-id="431ee-102">Prerequisites</span></span>

<span data-ttu-id="431ee-103">このフォルダーで完了したプロジェクトを実行するには、次のものが必要です。</span><span class="sxs-lookup"><span data-stu-id="431ee-103">To run the completed project in this folder, you need the following:</span></span>

- [<span data-ttu-id="431ee-104">Xcode</span><span class="sxs-lookup"><span data-stu-id="431ee-104">Xcode</span></span>](https://developer.apple.com/xcode/)
- [<span data-ttu-id="431ee-105">CocoaPods</span><span class="sxs-lookup"><span data-stu-id="431ee-105">CocoaPods</span></span>](https://cocoapods.org)
- <span data-ttu-id="431ee-106">Outlook.com 上のメールボックスを持つ個人の Microsoft アカウント、または Microsoft 職場または学校のアカウントのいずれか。</span><span class="sxs-lookup"><span data-stu-id="431ee-106">Either a personal Microsoft account with a mailbox on Outlook.com, or a Microsoft work or school account.</span></span>

> <span data-ttu-id="431ee-107">**注:** このチュートリアルは、Xcode バージョン11.4 と Cocoアポストロフィ Ds バージョン1.9.1 を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="431ee-107">**Note:** This tutorial was written using Xcode version 11.4 and CocoaPods version 1.9.1.</span></span> <span data-ttu-id="431ee-108">このガイドの手順は、他のバージョンでは動作しますが、テストされていません。</span><span class="sxs-lookup"><span data-stu-id="431ee-108">The steps in this guide may work with other versions, but that has not been tested.</span></span>

<span data-ttu-id="431ee-109">Microsoft アカウントを持っていない場合は、無料のアカウントを取得するためのオプションがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="431ee-109">If you don't have a Microsoft account, there are a couple of options to get a free account:</span></span>

- <span data-ttu-id="431ee-110">[新しい個人用 Microsoft アカウントにサインアップ](https://signup.live.com/signup?wa=wsignin1.0&rpsnv=12&ct=1454618383&rver=6.4.6456.0&wp=MBI_SSL_SHARED&wreply=https://mail.live.com/default.aspx&id=64855&cbcxt=mai&bk=1454618383&uiflavor=web&uaid=b213a65b4fdc484382b6622b3ecaa547&mkt=E-US&lc=1033&lic=1)することができます。</span><span class="sxs-lookup"><span data-stu-id="431ee-110">You can [sign up for a new personal Microsoft account](https://signup.live.com/signup?wa=wsignin1.0&rpsnv=12&ct=1454618383&rver=6.4.6456.0&wp=MBI_SSL_SHARED&wreply=https://mail.live.com/default.aspx&id=64855&cbcxt=mai&bk=1454618383&uiflavor=web&uaid=b213a65b4fdc484382b6622b3ecaa547&mkt=E-US&lc=1033&lic=1).</span></span>
- <span data-ttu-id="431ee-111">[Office 365 開発者プログラムにサインアップ](https://developer.microsoft.com/office/dev-program)して、無料の office 365 サブスクリプションを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="431ee-111">You can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.</span></span>

## <a name="register-a-web-application-with-the-azure-active-directory-admin-center"></a><span data-ttu-id="431ee-112">Web アプリケーションを Azure Active Directory 管理センターに登録する</span><span class="sxs-lookup"><span data-stu-id="431ee-112">Register a web application with the Azure Active Directory admin center</span></span>

1. <span data-ttu-id="431ee-113">ブラウザーを開き、[Azure Active Directory 管理センター](https://aad.portal.azure.com)へ移動します。</span><span class="sxs-lookup"><span data-stu-id="431ee-113">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com).</span></span> <span data-ttu-id="431ee-114">**個人用アカウント** (別名: Microsoft アカウント)、または**職場/学校アカウント**を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="431ee-114">Login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="431ee-115">左側のナビゲーションで **[Azure Active Directory]** を選択し、それから **[管理]** で **[アプリの登録]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="431ee-115">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

    ![<span data-ttu-id="431ee-116">アプリの登録のスクリーンショット</span><span class="sxs-lookup"><span data-stu-id="431ee-116">A screenshot of the App registrations</span></span> ](/tutorial/images/aad-portal-app-registrations.png)

1. <span data-ttu-id="431ee-117">**[新規登録]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="431ee-117">Select **New registration**.</span></span> <span data-ttu-id="431ee-118">**[アプリケーションを登録]** ページで、次のように値を設定します。</span><span class="sxs-lookup"><span data-stu-id="431ee-118">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="431ee-119">`iOS Swift Graph Tutorial` に **[名前]** を設定します。</span><span class="sxs-lookup"><span data-stu-id="431ee-119">Set **Name** to `iOS Swift Graph Tutorial`.</span></span>
    - <span data-ttu-id="431ee-120">**[サポートされているアカウントの種類]** を **[任意の組織のディレクトリ内のアカウントと個人用の Microsoft アカウント]** に設定します。</span><span class="sxs-lookup"><span data-stu-id="431ee-120">Set **Supported account types** to **Accounts in any organizational directory and personal Microsoft accounts**.</span></span>
    - <span data-ttu-id="431ee-121">**[リダイレクト URI]** を空のままにします。</span><span class="sxs-lookup"><span data-stu-id="431ee-121">Leave **Redirect URI** empty.</span></span>

    ![[アプリケーションを登録する] ページのスクリーンショット](/tutorial/images/aad-register-an-app.png)

1. <span data-ttu-id="431ee-123">**[登録]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="431ee-123">Choose **Register**.</span></span> <span data-ttu-id="431ee-124">[ **IOS Swift グラフ] チュートリアル**ページで、**アプリケーション (クライアント) ID**の値をコピーして保存します。次の手順で必要になります。</span><span class="sxs-lookup"><span data-stu-id="431ee-124">On the **iOS Swift Graph Tutorial** page, copy the value of the **Application (client) ID** and save it, you will need it in the next step.</span></span>

    ![新しいアプリ登録のアプリケーション ID のスクリーンショット](/tutorial/images/aad-application-id.png)

1. <span data-ttu-id="431ee-126">**[管理]** の下の **[認証]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="431ee-126">Select **Authentication** under **Manage**.</span></span> <span data-ttu-id="431ee-127">[**プラットフォームの追加**] を選択し、[ **iOS/macOS**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="431ee-127">Select **Add a platform**, then **iOS / macOS**.</span></span>

1. <span data-ttu-id="431ee-128">アプリのバンドル ID を入力し、[**構成**] を選択して、[**完了**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="431ee-128">Enter your app's Bundle ID and select **Configure**, then select **Done**.</span></span>

## <a name="configure-the-sample"></a><span data-ttu-id="431ee-129">サンプルを構成する</span><span class="sxs-lookup"><span data-stu-id="431ee-129">Configure the sample</span></span>

1. <span data-ttu-id="431ee-130">ファイルの`AuthSettings.plist.example`名前を`AuthSettings.plist`に変更します。</span><span class="sxs-lookup"><span data-stu-id="431ee-130">Rename the `AuthSettings.plist.example` file to `AuthSettings.plist`.</span></span>
1. <span data-ttu-id="431ee-131">`AuthSettings.plist`ファイルを編集し、次のように変更します。</span><span class="sxs-lookup"><span data-stu-id="431ee-131">Edit the `AuthSettings.plist` file and make the following changes.</span></span>
    1. <span data-ttu-id="431ee-132">を`YOUR_APP_ID_HERE`アプリ登録ポータルで取得した**アプリケーション Id**に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="431ee-132">Replace `YOUR_APP_ID_HERE` with the **Application Id** you got from the App Registration Portal.</span></span>
1. <span data-ttu-id="431ee-133">**Graphtutorial**ディレクトリでターミナルを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="431ee-133">Open Terminal in the **GraphTutorial** directory and run the following command.</span></span>

    ```Shell
    pod install
    ```

## <a name="run-the-sample"></a><span data-ttu-id="431ee-134">サンプルを実行する</span><span class="sxs-lookup"><span data-stu-id="431ee-134">Run the sample</span></span>

<span data-ttu-id="431ee-135">Xcode で、[**製品**] メニューを選択し、[**実行**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="431ee-135">In Xcode, select the **Product** menu, then select **Run**.</span></span>
