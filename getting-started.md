---
copyright:
  years: 2020, 2021
lastupdated: "2020-07-19"

keywords: 
subcollection: cognos-analytics

content-type: tutorial
services: 
account-plan: lite 
completion-time: 15m 
---

{:codeblock: .codeblock}  
{:note: .note}
{:pre: .pre}
{:shortdesc: .shortdesc}
{:screen: .screen}  
{:table: .aria-labeledby="caption"}
{:tip: .tip}
{:video: .video}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'} 

# Getting started with {{site.data.keyword.cognosanalytics_short}}
{: #getting-started}
{: toc-content-type="tutorial"} 
{: toc-services=""} 
{: toc-completion-time="10m"} 

In this getting started tutorial, use {{site.data.keyword.cognosanalytics_full}} (Experimental) to create a dashboard with interactive visualizations.
{: shortdesc}

For more tutorials, videos, and hands-on labs, see [IBM Demos: Cognos Analytics](https://www.ibm.com/demos/collection/IBM-Cognos-Analytics/).


<!--- Docs assume that the service has already been provisioned.
## Provisioning the service
{: #prereqs}
To create a {{site.data.keyword.cognosanalytics_short}} service instance, complete the following steps:

1. In your web browser, go to https://cloud.ibm.com/login.
2. Log in to your {{site.data.keyword.cloud}} account, or create an account.
3. Go to the {{site.data.keyword.cloud}} catalog: https://cloud.ibm.com/catalog.
4. In the `Services` section, select the `Analytics` category and then click the {{site.data.keyword.cognosanalytics_short}} tile.
5. On the {{site.data.keyword.cognosanalytics_short}} catalog page, specify the following information.
  - Specify a name for the new {{site.data.keyword.cognosanalytics_short}} service instance.
  - Choose a region.
  - Choose a resource group.
  - Choose the `Lite` planning price.
  - Click `Create`.

The {{site.data.keyword.cognosanalytics_short}} service instance page displays after the service instance is created. The page provides access the Getting Started documentation, create credentials, and view or change your plan settings.
-->

## Uploading data
{: #upload_data}
{: step}
Upload some sample data to use in this tutorial.
{: shortdesc}

1. Download the sample [HR_Training](https://www.ibm.com/support/knowledgecenter/SSEP7J_11.1.0/com.ibm.swg.ba.cognos.ug_ca_dshb.doc/IBM_HR_Training_2014-17.csv) CSV file to your local system.
2. In the {{site.data.keyword.cognosanalytics_short}} interface, click the `Open menu` icon ![Open menu](images/icon_open_menu.jpg "Open menu icon") and then click `Upload files`.
3. Go to the sample CSV file and select it. 
4. Click `Open`. The `My content` folder includes the uploaded file.

## Creating a dashboard
{: #create_dashboard}
{: step}
Create a dashboard with the sample data.

1. On the home page, click the `Open menu` icon ![Open menu](images/icon_open_menu.jpg "Open menu icon") and then click `New`.
2. Click `Dashboard`.
3. From the available templates, select the default template and click `Create`. 
4. In the `Data` pane, click `Select a source`.
5. Go to the `My content` folder and select <filepath>IBM_HR_Training_2014-17.csv</filepath>. 
6. Click `Add`.
7. From the data source, drag "Department" into the upper-left pane of your dashboard. You now see a list of departments.
8. From the data source, drag "External hires" onto the "Department" list. The list becomes a column chart, showing the Sales department with the most external hires.
9. Change the visualization type by clicking the column chart and then clicking the `Change visualization` icon in the toolbar.
10. Click `All visualizations` and select a different type, such as `Packed bubble`.
11. Try adding another visualization and explore the other data columns.
12. Finally, save the dashboard and then use the switcher in the application bar to close it. 

For more information, see [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/en/SSEP7J_11.1.0/com.ibm.swg.ba.cognos.ug_ca_dshb.doc/wa_dashboard_discoveryset_intro.html), [YouTube playlist](https://youtu.be/gYCGAD22sDE), or [Hands-on labs](https://www.ibm.com/demos/collection/IBM-Cognos-Analytics/).


## Assistant-generated dashboard
{: #generate_dashboard}
{: step}
Alternatively, you can use natural-language text to ask the embedded AI assistant to generate a dashboard.

1. Open a dashboard.
2. Click the `Assistant` icon ![Assistant](images/icon_assistant.jpg "Assistant icon").
3. In the `Ask a question` field, enter ```show data```.
4. Click the <filepath>IBM_HR_Training_2014-17.csv</filepath> data source.
5. Type ```create dashboard``` and click Enter. A dashboard is automatically created for you with chart selections based on the selected data source.

For more information, see 
[IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/en/SSEP7J_11.1.0/com.ibm.swg.ba.cognos.ug_ca_dshb.doc/c_assistant.html).

<!---
## Next steps
{: #anchor_value}

What's the single thing the user needs to do next? Think "guided journey." Either provide information that leads the user to production use, for example HA, how to make a service secure, or how to connect to on-premise data. Or you can point the user to another tutorial. Give a choice between two options max._
--->
