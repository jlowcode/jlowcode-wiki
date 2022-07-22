# Bagit Plugin
<h1 align="center">
  <img alt="Joomla" title="Joomla" src="img/logo.png" width="220px" />
</h1>

## 🚀 Specifications
<ul>
  <li>This is a form plugin that should work after the certificate plugin.</li>
   <li>Should work when user adds or edits a form from a fabrik record. After the after process function.</li>
   <li>It will generate a folder with the export of each record in bagit format.</li>
   <li>In the plugin settings there should be an option to configure the server folder where the log folders are generated.</li>
   <li>The objective is to generate a folder that can be ingested by the Archivematica software that guarantees another layer of assurance in digital preservation.</li>
   <li>The sha512 method must be used to generate the hash.</li>
</ul>

## 💻 Tutorial
<p>The 1st step is to configure the plugin.</p>

<p align="center">
  <img alt="First step" src="../imgens/bagitpasso_um.png" width="100%">
</p>

<p>Then configure each element respectively:</p>

<p align="center">
  <img alt="Second step" src="../imgens/bagitpasso_dois.png" width="100%">
</p>

<p><b>2</b>: Configures the temporary path where the log folders are generated.</p>
<p><b>3</b>: Sets the permanent path where the log folders are generated.</p>
<p><b>4</b>: You can configure a version for bagit.</p>
<p><b>5</b>: Select the certificate plugin.</p>
<p><b>6</b>: List element of the fileupload type that should have its files preserved.</p>

## 🔖 More

<p>To learn more about the generated file format, see:</p>

<ul>
  <li>https://docs.google.com/document/d/1dL9d-T5EisBkAhHdXfXBaa62j4t7SgDInLzIHpx-eNE/edit?usp=sharing</li>
  <li>https://tools.ietf.org/html/draft-kunze-bagit-17</li>
</ul>

<p>By exporting the record in this format and having it ingested by Archivematica, the long-term preservation of the information is guaranteed and there is another layer of protection against hackers.</p>

<ul>
  <li>https://www.archivematica.org/en/docs/archivematica-1.11/user-manual/transfer/bags/#bags</li>
</ul>

<p>A plugin that can be used as a template for this is the certificate plugin which does something similar: it exports the log to pdf.</p>

<ul>
  <li>https://github.com/pittufg/registration_certificate</li>
</ul>
Footer
© 2022 GitHub, Inc.
Footer navigation

    Terms
    Privacy
    Security
    Status
    Docs
