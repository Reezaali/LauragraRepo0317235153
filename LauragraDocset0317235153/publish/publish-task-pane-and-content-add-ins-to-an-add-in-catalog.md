
# Publish task pane and content add-ins to a SharePoint catalog

>**Important!** Add-in catalogs on SharePoint do not support add-in features that are implemented in the VersionOverrides node of the [add-in manifest](../overview/add-in-manifests.md), such as add-in commands. 

>If you’re targeting a cloud or hybrid environment, we recommend that you use **centralized deployment** via the [admin center (preview)](publish/publish.md#office-365-admin-center-preview-deployment) to publish your add-ins.

An add-in catalog is a dedicated site collection in a SharePoint web application or SharePoint Online tenancy that hosts document libraries for Office and SharePoint Add-ins. Administrators can upload Office Add-ins manifest files to the add-in catalog for their organization. When an administrator registers an add-in catalog as a trusted catalog, users can insert the add-in from the insertion UI in an Office client application.

SharePoint catalogs are not supported for Office 2016 for Mac. To deploy Office Add-ins to Mac clients, you must submit them to the [Office Store](http://msdn.microsoft.com/library/ff075782-1303-4517-91cc-b3d730e9b9ae%28Office.15%29.aspx).   

## To set up an add-in catalog on SharePoint

1. Browse to the  **Central Administration Site** ( **Start** > **All Programs** > **Microsoft SharePoint 2013 Products** > **SharePoint 2013 Central Administration**).
    
2. In the left task pane, choose  **Add-ins**.
    
3. On the  **Add-ins** page, under **Add-in Management**, choose  **Manage Add-in Catalog**.
    
4. On the  **Manage Add-in Catalog** page, make sure you have the right web application selected in the **Web Application Selector**.
    
5. Choose  **View site settings**.
    
6. On the  **Site Settings** page, choose **Site collection administrators** to specify the site collection administrators, and then choose **OK**.
    
7. To grant site permissions to users, choose  **Site Permissions**, and then choose  **Grant Permissions**.
    
8. In the  **Share 'App Catalog Site'** dialog box, specify one or more site users, set the appropriate permissions for them, optionally set other options, and then choose **Share**.
    
9. To add add-ins to the Office Add-ins add-in catalog, choose  **Office Add-ins**.

## To set up an add-in catalog on Office 365

1. On the Office 365 admin center page, choose  **Admin**, and then choose  **SharePoint**.
    
2. In the left task pane, choose  **add-ins**.
    
3. On the  **add-ins** page, choose **Add-in Catalog**.
    
4. On the  **Add-in Catalog Site** page, choose **OK** to accept the default option and create a new add-in catalog site.
    
5. On the  **Create Add-in Catalog Site Collection** page, specify the title of your Add-in Catalog site.
    
6. Specify the web site address.
    
7. Set the  **Storage Quota** to the lowest possible value (currently 110). You will only be installing add-in packages on this site collection and they are very small.
    
8. Set the  **Server Resource Quota** to 0 (zero). (The server resource quota is related to throttling poorly performing sandboxed solutions, but you won't be installing any sandboxed solutions on your add-in catalog site.)
    
9. Choose  **OK**.
    
To add add-in to the Add-in Catalog Site, browse to the site you have just created. In the left navigation pane, choose  **Office Add-ins**, and then, to upload an Office Add-in manifest file, choose  **new add-in**.    

## Publish to an add-in catalog


1. Browse to the add-in catalog:

	1- Open the SharePoint Central Administration main page.
	
	2- Select  **Add-ins**.
	
	3- Select  **Manage Add-in Catalog**.
	
	4- Choose the link provided, and then choose  **Office Add-ins** on the left navigation bar.
    
2. Choose the  **Click to add new item** link.
    
3. Choose  **Browse**, and then specify the [manifest](../../docs/overview/add-in-manifests.md) to upload.
    
    Content and task pane add-ins in this catalog are now available from the  **Office Add-ins** dialog box. To access them, choose **My Add-ins** on the **Insert** tab, and then choose **MY ORGANIZATION**.
    
After you upload add-in manifests to the Office Add-ins catalog, users can access the add-ins by doing the following:


1. In the Office application, go to  **File** > **Options** > **Trust Center** > **Trust Center Settings** > **Trusted Add-in Catalogs**.
    
2. Specify the URL of the  _parent SharePoint site collection_ of the add-in catalog. For example, if the URL of the Office Add-ins catalog is:
    
    `https:// _domain_ /sites/ _AddinCatalogSiteCollection_ /AgaveCatalog`
    
    Specify just the URL of the parent site collection:
    
    `https:// _domain_ /sites/ _AddinCatalogSiteCollection_`
    
3. Close and reopen the Office application. The add-in catalog will be available in the  **Office Add-ins** dialog box.
    
Alternatively, an administrator can specify an Office Add-in catalog on SharePoint by using group policy. For details, see the section "Using Group Policy to manage how users can install and use Office Add-ins" in [Overview of Office Add-ins](https://technet.microsoft.com/en-us/library/jj219429.aspx) on TechNet.

