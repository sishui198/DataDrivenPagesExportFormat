<h1 class="gpHeading" xmlns="">DDPExportTools</h1>
<h2 class="gp" xmlns="">Title 
		<span class="gpsubtitle">DDPExportTools</span>
</h2>
<h2 class="gp" xmlns="">Summary</h2>
<div class="gpItemInfo" xmlns="">
<p><DIV STYLE="text-align:Left;"><DIV><DIV><P><SPAN>This scripting tool is designed to take a selected MXD, and export all of its Data Driven Pages as the specified file format (PNG,JPEG, etc.) for map and infographic creation. </SPAN></P></DIV></DIV></DIV></p><br />
</div>
<h2 class="gp" xmlns="">Usage</h2>
<div class="gpItemInfo" xmlns="">
<p><DIV STYLE="text-align:Left;"><DIV><DIV><P><SPAN>The goal of this script is to make accessible other export formats for data driven pages. Specifically this toolkit intends to help provide opportunities for using datadriven pages for easy </SPAN><A href="http://visual.ly/beginners-guide-image-formats-web"><SPAN>infographic creation </SPAN></A><SPAN>without having to leave ArcGIS to get a usable end product (no batch PDF conversions). </SPAN></P></DIV></DIV></DIV></p><br />
</div>
<h2 class="gp" xmlns="">Syntax</h2>
<div xmlns="">
<p style="margin-top: -1.2em">DDPExportPNG (Input_Map_Document, Base_Name, Output_Directory, DPI_Resolution) <br /><br />
</p>
<table width="100%" border="0" cellpadding="5">
<tbody>
<tr>
<th width="30%">
<b>Parameter</b>
</th>
<th width="50%">
<b>Explanation</b>
</th>
<th width="20%">
<b>Data Type</b>
</th>
</tr>
<tr>
<td class="info">Input_Map_Document</td>
<td class="info" align="left">
<span style="font-weight: bold">Dialog Reference</span><br /><DIV STYLE="text-align:Left;"><DIV><P><SPAN>This is the map document whose data driven pages will be used to export into you final images. </SPAN></P></DIV></DIV><div class="noContent" style="text-align:center; margin-top: -1em">___________________</div><br />
<span style="font-weight: bold">Python Reference</span><br /><DIV STYLE="text-align:Left;"><DIV><P><SPAN>Is the MXD Path that is passed to the arcpy mapping library functions for dealing with MXDs. </SPAN></P></DIV></DIV></td>
<td class="info" align="left">File</td>
</tr>
<tr>
<td class="info">Base_Name</td>
<td class="info" align="left">
<span style="font-weight: bold">Dialog Reference</span><br /><DIV STYLE="text-align:Left;"><DIV><P><SPAN>This is the base name that all of the new images will have at the beginning of their file names. Files are exported in the format: Base_Name+_+PageNumber.</SPAN></P><P><SPAN /></P></DIV></DIV><div class="noContent" style="text-align:center; margin-top: -1em">___________________</div><br />
<span style="font-weight: bold">Python Reference</span><br /><DIV STYLE="text-align:Left;"><P STYLE="font-size:12ptmargin:0 0 0 0;"><SPAN><SPAN>PageName</SPAN></SPAN><SPAN STYLE="font-weight:bold;"><SPAN>=</SPAN></SPAN><SPAN><SPAN>"{0}_{1}"</SPAN></SPAN><SPAN><SPAN>.format(</SPAN></SPAN><SPAN><SPAN>str</SPAN></SPAN><SPAN><SPAN>(</SPAN></SPAN><SPAN STYLE="font-style:italic;"><SPAN>base_name</SPAN></SPAN><SPAN><SPAN>),</SPAN></SPAN><SPAN><SPAN>str</SPAN></SPAN><SPAN><SPAN>(PageEnd))</SPAN></SPAN></P></DIV></td>
<td class="info" align="left">String</td>
</tr>
<tr>
<td class="info">Output_Directory</td>
<td class="info" align="left">
<span style="font-weight: bold">Dialog Reference</span><br /><DIV STYLE="text-align:Left;"><DIV><P><SPAN>This is the output directory you want your image files to exported to. </SPAN></P></DIV></DIV><div class="noContent" style="text-align:center; margin-top: -1em">___________________</div><br />
<span style="font-weight: bold">Python Reference</span><br /><DIV STYLE="text-align:Left;"><P STYLE="font-size:12ptmargin:0 0 0 0;"><SPAN><SPAN>out_file</SPAN></SPAN><SPAN STYLE="font-weight:bold;"><SPAN>=</SPAN></SPAN><SPAN><SPAN>os.path.join(</SPAN></SPAN><SPAN STYLE="font-style:italic;"><SPAN>out_dir</SPAN></SPAN><SPAN><SPAN>,</SPAN></SPAN><SPAN><SPAN>"{0}.{1}"</SPAN></SPAN><SPAN><SPAN>.format(</SPAN></SPAN><SPAN><SPAN>PageName</SPAN></SPAN><SPAN><SPAN>,extension))</SPAN></SPAN></P><DIV><P><SPAN /></P></DIV></DIV></td>
<td class="info" align="left">Folder</td>
</tr>
<tr>
<td class="info">DPI_Resolution</td>
<td class="info" align="left">
<span style="font-weight: bold">Dialog Reference</span><br /><DIV STYLE="text-align:Left;"><DIV><P><SPAN>This is the dots per square inch resolution of your images. The export will default to the page lay out for the outputs width and length parameters. </SPAN></P></DIV></DIV><div class="noContent" style="text-align:center; margin-top: -1em">___________________</div><br />
<span style="font-weight: bold">Python Reference</span><br /><DIV STYLE="text-align:Left;"><DIV><P><SPAN>See Export Format Functions for details: http://desktop.arcgis.com/en/arcmap/10.3/analyze/arcpy-mapping/exportreport.htm</SPAN></P><P><SPAN /></P></DIV></DIV></td>
<td class="info" align="left">Long</td>
</tr>
</tbody>
</table>
</div>
<h2 class="gp" xmlns="">Code Samples</h2>
<div class="gpItemInfo" xmlns="">
<p><span class="noContent">There are no code samples for this tool.</span></p>
</div>
<h2 class="gp" xmlns="">Tags</h2>
<div class="gpItemInfo" xmlns="">
<p>ArcGIS, Data Driven Pages, Infographics, Web Pop Ups, Image, Formats</p>
</div>
<h2 class="gp" xmlns="">Credits</h2>
<div class="gpItemInfo" xmlns="">
<p>
<p>David Wasserman</p>
</p><br />
</div>
<h2 class="gp" xmlns="">Use limitations</h2>
<div class="gpItemInfo" xmlns="">
<p><DIV STYLE="text-align:Left;"><DIV><DIV><P><SPAN>This scripting tool will only work for ArcGIS 10.X. Pro has a completely different mapping library that would need to be addressed before being applicable. </SPAN></P></DIV></DIV></DIV></p><br />
</div>
</body>
</html>
