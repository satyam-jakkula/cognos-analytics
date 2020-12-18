---

copyright:
  years: 2020, 2020
lastupdated: "2020-09-17"

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

# About
{{site.data.keyword.cognosanalytics_long}} is an AI-fueled business intelligence solution that supports the entire analytics cycle, from discovery to operationalization. Visualize, analyze, and share actionable insights about your data with anyone in your organization.

Visualize and share your business performance and insights in dashboards and reports. Embedded AI helps you uncover hidden patterns in your data and presents actionable insights in plain language. Cleanse and combine your data sources in minutes with AI-assisted data preparation.

To see an example of a {{site.data.keyword.cognosanalytics_short}} dashboard, go to [IBM Global COVID-19 Statistics](https://accelerator.weather.com/bi/?boardId=iC2B38B09B142481EB83935F6419CA837) or browse the [IBM Data and AI Accelerators](https://community.ibm.com/accelerators/?context=analytics&product=Cognos%20Analytics) catalog for various samples that pertain to your industry.

## Terminology
{: #terminology}
The following table includes terms that are used in {{site.data.keyword.cognosanalytics_short}}.
| Term | Description |
| --------- | ------------------- |
| Column | An element of a data tree when relational data is used as a source, most often in modeling. The equivalent in other components is a field. |
| Dashboard | A web page that can contain one or more widgets that graphically represent business data. |
| Data module | A data source that fuses together multiple sources of data, including relational and OLAP databases, Hadoop-based technologies, Excel spreadsheets, text files, and more. Dashboards, reports, stories, and explorations use data modules as their sources. |
| Data source | The source of data itself, such as a database or XML file, and the connection information necessary for accessing the data. |
| Exploration | A flexible workspace where you can discover and analyze data. Uncover hidden relationships and identify patterns. |
| Field | An element of a data tree in an analysis, which can refer to both relational and dimensional data. A field can represent columns and cube objects, such as levels and hierarchies. The equivalent in other components is a column. |
| Report | A set of data deliberately laid out to communicate business information. |
| Story | A presentation format for your data analysis and insights; composed of a set of scenes that are displayed in sequence over time. |
{: caption="Table 1. {{site.data.keyword.cognosanalytics_short}} Terms" caption-side="bottom"}


<!---
{{site.data.keyword.cognosanalytics_short}} is experimental. Experimental services might be unstable or change frequently. Be aware of [experimental limitations](/docs/codeengine?topic=codeengine-kn-limits#kn-limits_experimental).
{: preview}
--->

# Getting started with {{site.data.keyword.cognosanalytics_short}}
{: #getting-started}
{: toc-content-type="tutorial"} <!-- Always use this value -->
{: toc-services=""} <!-- Use same value from services metadata above - that is, in most cases, leave empty. -->
{: toc-completion-time="10m"} <!-- Use same value from completion-time metadata above -->

In this getting started tutorial, use {{site.data.keyword.cognosanalytics_long}} (Experimental) to create a dashboard with interactive visualizations.
{: shortdesc}

For more tutorials, videos, and hands-on labs, see [IBM Demos: Cognos Analytics](https://www.ibm.com/demos/collection/IBM-Cognos-Analytics/).

Watch this video to see an introduction to the {{site.data.keyword.cognosanalytics_short}}.
![Introduction to Cognos Analytics](https://www.youtube.com/embed/krh-VahdOmc?rel=0){: video output="iframe" data-script="none" id="youtubeplayer1" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen}

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

<!-- For each step in your tutorial, add an H2 section. The title should be task-oriented and descriptive. Recommendation is no more than 9 steps. -->

## Uploading data
{: #upload_data}
{: step}
Upload some sample data to use in this tutorial.
{: shortdesc}

1. Download the sample [HR_Training](https://www.ibm.com/support/knowledgecenter/SSEP7J_11.1.0/com.ibm.swg.ba.cognos.ug_ca_dshb.doc/IBM_HR_Training_2014-17.csv) CSV file to your local system.
2. In the {{site.data.keyword.cognosanalytics_short}} interface, click `New` and then click `Upload files`.
3. Go to the sample CSV file and select it. The data appears in the `My content` folder.
4. Click `OK`.

<!---
## Creating a dashboard
{: #create_dashboard}
{: step}
Create a dashboard with the sample data.

1. On the home page, click the `New` icon.
2. Click `Dashboard`.
3. From the available templates, select the template with four panes and click `OK`. 
4. In the `Data` window, click the `Add a source` icon.
5. Go to the `My content` folder and select <filepath>IBM_HR_Training_2014-17.csv</filepath>. 
6. Click `Add`.
7. From the data source, drag "Department" into the upper-left pane of your dashboard. You now see a list of departments.
8. From the data source, drag "External hires" onto the "Department" list. The list becomes a column chart, showing the Sales department with the most external hires.
9. Change the visualization type by clicking the column chart and then clicking the `Change visualization` icon in the toolbar.
10. Click `All visualizations` and select a different type, such as `Packed bubble`.
11. Try adding another visualization and explore the other data columns.
12. Finally, save the dashboard and then use the switcher in the application bar to close it. 

### Assistant-generated dashboard
{: #create_dashboard}
{: step}
Alternatively, you can use natural-language text to ask the embedded AI assistant to generate a dashboard.

1. Open the sample dashboard.
2. Click the `Assistant` icon.
3. Type ```show data``` in the Assistant pane and click Enter.
4. Click the <filepath>IBM_HR_Training_2014-17.csv</filepath> data source.
5. Type ```create dashboard``` and click Enter. A dashboard is automatically created for you with chart selections based on the selected data source.


## Creating a story
{: #create_report}
{: step}

## Creating an exploration
{: #create_exploration}
{: step}

## Creating a report
{: #anchor_value}
{: step}


_If you have any "tips" to include for this step, add the content in the flow where you would like it to appear. This information should be not be required information for completing the step, but helpful information in explaining additional concepts about what the user is doing in the step. It should be in the following format:_

One to two sentences of content that can include inline links or lists.
{: tip}

_You can have multiple "tips" per step. Each tip will output with a *Tip:* label and be formatted in a nested, styled box._

## Next steps
{: #anchor_value}

_What's the single thing the user needs to do next? Think "guided journey." Either provide information that leads the user to production use, for example HA, how to make a service secure, or how to connect to on-premise data. Or you can point the user to another tutorial. Give a choice between two options max._
--->
