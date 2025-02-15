---
nav_title: Export Segment Data to CSV
article_title: Export Segment Data to CSV
page_order: 2
page_type: reference
description: "This reference article covers how to export segment data to CSV."

---

# Exporting to CSV

To request a CSV export of user data from a segment, click the **User Data** dropdown while editing a segment and select to export either the user data or email addresses for the segment.

![][1]

You can also request a CSV export from the main **Segments** page by clicking the <i class="fas fa-gear"></i> **Settings** dropdown for a segment:

![][2]

The CSV output contains the data from each user profile captured in the segment at the time of export. You can export any segment by clicking the gear icon and CSV export. Braze will generate the report in the background and email it to the user who is currently logged in.

{% alert important %} 
Due to file size restrictions, your export may fail if the estimated size of your segment is over 500,000 users. Note that this restriction uses the estimated size of your segment, and not the exact calculation. For more details, see [Exporting large segments]({{site.baseurl}}/help/help_articles/segments/exporting_large_segments/).
{% endalert %}

If you've linked your [Amazon S3 credentials][26] to Braze, the CSV will instead be uploaded in your S3 bucket under the key `segment-export/SEGMENT_ID/YYYY-MM-dd/users-RANDOMSTRING.zip`. The link emailed to you will expire after one day of exporting and requires that you are logged into the dashboard for access.

Data included in the exports:

- All User Data
    - User ID
    - First Name
    - Last Name
    - Time zone
    - City
    - Gender
    - Email Address
    - Phone Number
    - Number of Push Tokens
    - Twitter Username
    - Session Count
    - First Session
    - Last Session
    - Last App Version Used
    - In-App Purchase Total
    - Email Unsubscribe Time 
    - Device Info
    - Number of IDFAs
    - Number of IDFVs
    - Custom Events
    - Custom Attributes
- Email Addresses
    - User ID
    - First Name
    - Last Name
    - Email Address
    - Email Unsubscribe Date
    - Email Opt-in Date

{% alert tip %}
For help with CSV and API exports, visit our [troubleshooting]({{site.baseurl}}/user_guide/data_and_analytics/export_braze_data/export_troubleshooting/) article.
{% endalert %} 

[1]: {% image_buster /assets/img_archive/csvexport.png %}
[2]: {% image_buster /assets/img_archive/csvexport2.png %}
[26]: {{site.baseurl}}/partners/data_and_infrastructure_agility/data_warehouses/amazon_s3/#amazon-s3-integration
