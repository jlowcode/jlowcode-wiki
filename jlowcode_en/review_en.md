# Plugin Review

![Joomla Badge](https://img.shields.io/badge/Joomla-5091CD?style=for-the-badge&logo=joomla&logoColor=white) ![PHP Badge](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)


## Content


- [Plugin](#plugin)
- [Database Collaboration](#collaboration)

## Plugin

The Form Review plugin. How to use and add it to the form.

### Access the form you want to add it to and click on the "Plugin" tab
<p align="center">
    <img src="../images/review01.jpeg">
</p>

### Click on the "Add" button
<p align="center">
    <img src="../images/review02.jpeg">
</p>

### Plugin Settings
<p align="center">
    <img src="../images/review03.jpeg">
</p>

<div id="colaboracao">
    <h1>Database Collaboration</h1>
</div>

- <b>Plugin Review when running:</b>
    - Copy master record id to id_master field
     - Change master record status to Revised
     - Replace in the (original) master record your ID with a new ID (CAUTION DOING THIS THROUGH SQL)
     - Replace in all repeat tables the relationships changing the ID of the record that was master by the new ID
     - Replace in all tables repeat the relationships by changing the ID of the candidate record approved by the ID_master
     - Replace your ID with ID_master in the approved candidate record (Just one update)

<p align="center">
    <img src="../images/review04.jpeg">
</p>

<p align="center">
    <img src="../images/review05.jpeg">
</p>
