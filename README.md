# Habpanel / Xiaomi Humidity Temperature Pressure sensor 
Widget designed for 2x2 habpanel dashboard grid <br>
<b>Note:</b> Use 100% of browser zoom
<hr>

<img src="https://github.com/andreypopov/habpanel-widget-xiaomi-sensor_weather_v1/blob/master/readme/widget_view1.png?raw=true" height="200">

<hr style="clear:both;">
<br>
<br>
<b>things/*.things</b> file:<br>
<code>
Thing mihome:sensor_weather_v1:YOUR ID "Xiaomi Temperature Sensor" [itemId="YOUR ID"]
</code>
<br>
<br>
<b>items/*.items</b> file:<br>
<code>//Xiaomi Temperature and Humidity Sensor<br>
Number HT_Temperature "Temperature" <temperature> { channel="mihome:sensor_weather_v1:YOUR ID:temperature" }<br>
Number HT_Humidity "Humidity" <humidity> { channel="mihome:sensor_weather_v1:YOUR ID:humidity" }<br>
Number HT_Pressure "Pressure"  { channel="mihome:sensor_weather_v1:YOUR ID:pressure" }<br>
Number HT_Battery "Battery" <battery> { channel="mihome:sensor_weather_v1:YOUR ID:batteryLevel" }<br>
Switch HT_BatteryLow "Battery Low" <energy> { channel="mihome:sensor_weather_v1:YOUR ID:lowBattery" }<br>
</code>
<br>
<br>
<b>sitemaps/*.sitemap</b> file:<br>
<code>Frame label="Xiaomi Huidity Sensor" {<br>
&nbsp;&nbsp;&nbsp;Text item=HT_Temperature label="Temperature [%.1f °C]" <br>
&nbsp;Text item=HT_Humidity label="Humidity [%.1f %%]" icon="humidity"<br>
&nbsp;Text item=HT_Pressure label="Pressure [%.1f kPa]" icon="pressure"<br>
&nbsp;Text item=HT_Battery label="Battery [%s %%]"<br>
}</code>
<br>
<br>
<b>persistence/mysql.persist</b> file:<br>
<code>HT_Temperature : strategy = everyChange, everyDay, restoreOnStartup<br>
HT_Humidity : strategy = everyChange, everyDay, restoreOnStartup<br>
HT_Pressure : strategy = everyChange, everyDay, restoreOnStartup<br>
HT_Battery : strategy = everyChange, everyDay, restoreOnStartup<br></code>



<span style="float:left;">
<img src="https://github.com/andreypopov/habpanel-widget-xiaomi-sensor_weather_v1/blob/master/readme/widget_settings1.png?raw=true" height="200">
</span>
<span style="float:left;">
<img src="https://github.com/andreypopov/habpanel-widget-xiaomi-sensor_weather_v1/blob/master/readme/device.jpg?raw=true" height="200">
</span>