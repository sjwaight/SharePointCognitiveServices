# Enriching SharePoint Image Libraries with Azure Cognitive Services

Azure Logic App demonstrating how you can enrich image data in SharePoint using Azure Cognitive Services.

See the corresponding blog and video that goes over this in detail.

You will need access to the following in order to use this code:

- A SharePoint Online (or SharePoint on-premises) Document Library to which you can authenticate a [Logic App SharePoint Connector](https://docs.microsoft.com/en-us/azure/connectors/connectors-create-api-sharepoint).
- An Azure Subscription (Trial or Paid) - sign-up for your free trial at [http://azure.com/free](http://azure.com/free). This demo will run happily within a Trial account.
- Images against which you can train a Custom Vision classifier. The [Open Images Dataset](https://storage.googleapis.com/openimages/web/index.html) is a good starting point.

You will need to edit the template.json file and replace the following placeholders:

- 'https://YOURTENANT.sharepoint.com/sites/YOURSITE': replace YOURTENANT and YOURSITE with the appropriate values for your SharePoint Online enviornment.
- '00000000-0000-0000-0000-000000000001': replace with the GUID of your actual target Document Library (you can easily view this by opening the List Settings page - the GUID is in the URL.
- '00000000-0000-0000-0000-000000000002': replace with the Project ID of your custom classifier in Azure Cognitive Service Custom Vision.
- '00000000-0000-0000-0000-000000000003': replace with your Subscription ID.

Note that it's likely you can deploy the Logic App but there will be problems because the connections for SharePoint Online or Cognitive Services are not included in the definition though they are referenced.
