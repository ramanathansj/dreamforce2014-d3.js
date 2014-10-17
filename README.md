  <h1>Dreamforce 2014 – Introduction to D3.js</h1>
  
  This repo contain source code for Dreamforce 2014 Talk “Introduction to D3.js”, contains the following demo codes
  <ul>
  <li>Draw Circle</li>
  <li>Dynamic Circle – Data Joins</li>
  <li>Bar Chart </li>
  <li>Line Chart </li>
  <li>Analytics API Tree Chart </li>
  <li>Conversion Analysis</li>

<br/>
Please find the link below for unmanaged package to install in your salesforce.com org
https://login.salesforce.com/packaging/installPackage.apexp?p0=04tU0000000ILHz

<h4>Slide deck</h4>
https://www.scribd.com/doc/243267456/Introduction-to-D3-js

<h4>Report</h4>
Make sure you have deployed the report called “Dreamforce2014” which is used as backend data source for Bar, Line, Tree charts so without it, you may get errors. This chart is available in report folder.

<h4>Note</h4>
You need appropriate data for line/bar chart, there is same data in this repo it needs to be imported or you need to have good amount of data which is distributed over period of time. If you are importing data use data loader and make necessary mapping to account though it is not required for charting.


<h4>Design Notes</h4>

<ul>
<li>One page load we execute a soql query to get report id of "Dreamforce2014" report using Forcetk Client Library</li>
<li>Call the reporting api to get Dreamforce2014 report metadata and data on callback success from previous step </li>
<li>We process and store this data in google charts datatable which is another library for charting but I'm using it as client side storage which reporesents a matrix like data structure with apis to slice/dice the data. Since there is good client storage solution available at this point I have to stick with this, I looked at indexDb I feel its lot of code to do simple things. </li>
<li>Twitter Bootstrap is used for designing layouts, etc </li>
<li> I have event handler function which invokes corresponding chart functions when the relevant chart list items are clicked </li>
</ul>


