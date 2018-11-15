<!-- default file list -->
*Files to look at*:

* [Form1.cs](./CS/Form1.cs) (VB: [Form1.vb](./VB/Form1.vb))
<!-- default file list end -->
# How to represent the PivotGridControl's data within XtraCharts


<p><strong>UPD: This example is outdated</strong><strong>. Please</strong><strong> see </strong><a href="https://www.devexpress.com/Support/Center/p/E2911">E2911</a><strong> for</strong><strong> an</strong><strong> </strong><strong>up-to-date </strong><strong>sample</strong><strong>.</strong><strong><br />
</strong><br />
To obtain the summary datasource generated by the PivotGridControl you should call its <strong>CreateSummaryDataSource</strong> method. Then, this datasource should be assigned to the <strong>ChartControl.DataSource</strong> property, and specify what data fields should be considered as series (<strong>SeriesDataMember</strong> property), what as series points arguments (<strong>SeriesTemplate.ArgumentDataMember</strong> property), and what as series points values (<strong>SeriesTemplate.ValueDataMembers</strong>).</p><p>In the following example the pivotGridControl1 is bound to the Northwind Traders datasource (nwind.mdb sample database) and shows sales data on products of different categories per years and months. Then, this data will be shown within a chartControl1 for the particular Category ("Beverages") and Year (1994). Also, the OptionsDataField.FieldNaming property value is DevExpress.XtraPivotGrid.DataFieldNaming.Name. This was done to differentiate between two OrderMonth columns with different GroupIntervals.</p>

<br/>


