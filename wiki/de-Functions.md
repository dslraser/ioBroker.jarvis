# Gewerke

Die Gewerke definierten den Typs eines Geräts, z. B. Licht oder Heizung. 

Grundsätzlich kann durch den Benutzer in Jarvis alles frei definiert und konfiguriert werden. Die Gewerke liefern hierzu bestimmte Voreinstellungen als Grundlage (die jedoch überschrieben werden können).

*Hinweis*: Die Spalten der unten dargestellten Tabellen sind unter [Geräte](./de-Devices#konfiguration-der-datenpunkte--states) erläutert.


# Übersicht der Gewerke
- [Rollladen / Jalousie](#gewerk-rollladen--jalousie-blind)
- [Tür](#gewerk-tür-door)
- [Lüfter](#gewerk-lüfter-fan)
- [Heizung](#gewerk-heizung-heating)
- [Licht](#gewerk-licht-light)
- [Ort](#gewerk-ort-location)
- [Bewegungs-/Präsenzmelder](#gewerk-bewegungs-präsenzmelder-motion)
- [Rasenmäher-Roboter](#gewerk-rasenmäher-roboter-mower)
- [Sensor](#gewerk-sensor-sensor)
- [Server](#gewerk-server-server)
- [Rauchmelder](#gewerk-rauchmelder-smoke)
- [Steckdose](#gewerk-steckdose-socket)
- [Lautsprecher](#gewerk-lautsprecher-speaker)
- [Fernseher](#gewerk-fernseher-tv)
- [Benutzer](#gewerk-benutzer-user)
- [Staubsauger-Roboter](#gewerk-staubsauger-roboter-vacuum)
- [Wetter-Station](#gewerk-wetter-station-weather-station)
- [Fenster](#gewerk-fenster-window)
- [Sonstige](#gewerk-sonstige-_defaults)


<h2>Gewerk Rollladen / Jalousie (<code>blind</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"window-shutter"</pre></td><td>-</td></tr>
<tr><td><code>level</code></td><td>-</td><td>-</td><td><code>%</code></td><td><pre lang="json">{
   "default": "window-shutter-open",
   ">90": "window-shutter-open",
   "<=90": "window-shutter"
}</pre></td><td>-</td></tr>
<tr><td><code>level2</code></td><td>-</td><td>-</td><td><code>%</code></td><td><pre lang="json">{
   "default": "window-shutter-open",
   ">90": "window-shutter-open",
   "<=90": "window-shutter"
}</pre></td><td>-</td></tr>
<tr><td><code>activity</code></td><td>-</td><td><pre lang="json">{
   "true": "in Bewegung",
   "false": "keine"
}</pre></td><td>-</td><td><pre lang="json">{
   "true": "pan-vertical",
   "false": "dots-vertical"
}</pre></td><td>-</td></tr>
</table>
<h3>Beispielkonfiguration</h3>
<h4>Adapter hm-prc</h4>
<h5>hmip-broll</h5>
<ul>
<li><code>level</code>
<ul>
<li>state: <code>.3.LEVEL</code></li>
<li>action: <code>.4.LEVEL</code></li>
</ul>
<li><code>level2</code>
<ul>
<li>state: <code>.3.LEVEL2</code></li>
<li>action: <code>.4.LEVEL2</code></li>
</ul>
<li><code>activity</code>
<ul>
<li>state: <code>.3.ACTIVITY_STATE</code></li>
<li>action: <code>.4.STOP</code></li>
</ul>
</ul>
<h5>hm-lc-bl1-fm</h5>
<ul>
<li><code>level</code>
<ul>
<li>state: <code>.1.LEVEL</code></li>
<li>action: <code>.1.LEVEL</code></li>
</ul>
<li><code>activity</code>
<ul>
<li>state: <code>.1.WORKING</code></li>
<li>action: <code>.1.STOP</code></li>
</ul>
</ul>
<h5>hm-lc-bl1pbu-fm</h5>
<ul>
<li><code>level</code>
<ul>
<li>state: <code>.1.LEVEL</code></li>
<li>action: <code>.1.LEVEL</code></li>
</ul>
<li><code>activity</code>
<ul>
<li>state: <code>.1.WORKING</code></li>
<li>action: <code>.1.STOP</code></li>
</ul>
</ul>
<h4>Adapter shelly</h4>
<ul>
<li><code>level</code>
<ul>
<li>state: <code>.Shutter.Position</code></li>
<li>action: <code>.Shutter.Position</code></li>
</ul>
<li><code>activity</code>
<ul>
<li>state: <code>.Shutter.state</code></li>
<li>action: <code>.Shutter.Pause</code></li>
</ul>
</ul>

<h2>Gewerk Tür (<code>door</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"door"</pre></td><td>-</td></tr>
<tr><td><code>open</code></td><td>-</td><td><pre lang="json">{
   "true": "offen",
   "false": "geschlossen"
}</pre></td><td>-</td><td><pre lang="json">{
   "true": "door-open",
   "false": "door-closed"
}</pre></td><td>-</td></tr>
<tr><td><code>lock</code></td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td></tr>
</table>

<h2>Gewerk Lüfter (<code>fan</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"fan"</pre></td><td>-</td></tr>
<tr><td><code>power</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">{
   "true": "fan",
   "false": "fan-off"
}</pre></td><td>-</td></tr>
</table>

<h2>Gewerk Heizung (<code>heating</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"radiator"</pre></td><td>-</td></tr>
<tr><td><code>temperature</code></td><td>-</td><td>-</td><td><code>°C</code></td><td><pre lang="json">"radiator"</pre></td><td>-</td></tr>
<tr><td><code>settemperature</code></td><td>-</td><td>-</td><td><code>°C</code></td><td><pre lang="json">"thermometer-chevron-up"</pre></td><td>-</td></tr>
<tr><td><code>humidity</code></td><td>-</td><td>-</td><td><code>%</code></td><td>-</td><td>-</td></tr>
<tr><td><code>boost</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"radiator"</pre></td><td>-</td></tr>
</table>
<h3>Beispielkonfiguration</h3>
<h4>Adapter hm-prc</h4>
<h5>hmip-bwth</h5>
<ul>
<li><code>temperature</code>
<ul>
<li>state: <code>.1.ACTUAL_TEMPERATURE</code></li>
</ul>
<li><code>setTemperature</code>
<ul>
<li>state: <code>.1.SET_POINT_TEMPERATURE</code></li>
<li>action: <code>.1.SET_POINT_TEMPERATURE</code></li>
</ul>
<li><code>humidity</code>
<ul>
<li>state: <code>.1.HUMIDITY</code></li>
</ul>
<li><code>boost</code>
<ul>
<li>state: <code>.1.BOOST_MODE</code></li>
<li>action: <code>.1.BOOST_MODE</code></li>
</ul>
</ul>
<h5>hmip-wth-2</h5>
<ul>
<li><code>temperature</code>
<ul>
<li>state: <code>.1.ACTUAL_TEMPERATURE</code></li>
</ul>
<li><code>setTemperature</code>
<ul>
<li>state: <code>.1.SET_POINT_TEMPERATURE</code></li>
<li>action: <code>.1.SET_POINT_TEMPERATURE</code></li>
</ul>
<li><code>humidity</code>
<ul>
<li>state: <code>.1.HUMIDITY</code></li>
</ul>
<li><code>boost</code>
<ul>
<li>state: <code>.1.BOOST_MODE</code></li>
<li>action: <code>.1.BOOST_MODE</code></li>
</ul>
</ul>
<h5>hm-cc-rt-dn</h5>
<ul>
<li><code>temperature</code>
<ul>
<li>state: <code>.4.ACTUAL_TEMPERATURE</code></li>
</ul>
<li><code>setTemperature</code>
<ul>
<li>state: <code>.4.SET_TEMPERATURE</code></li>
<li>action: <code>.4.SET_TEMPERATURE</code></li>
</ul>
<li><code>boost</code>
<ul>
<li>state: <code>.4.BOOST_MODE</code></li>
<li>action: <code>.4.BOOST_MODE</code></li>
</ul>
</ul>
<h4>Adapter hmip</h4>
<h5>hmip-etrv-2</h5>
<ul>
<li><code>temperature</code>
<ul>
<li>state: <code>.channels.1.valveActualTemperature</code></li>
</ul>
<li><code>setTemperature</code>
<ul>
<li>state: <code>.channels.1.setPointTemperature</code></li>
<li>action: <code>.channels.1.setPointTemperature</code></li>
</ul>
</ul>

<h2>Gewerk Licht (<code>light</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"lightbulb-on"</pre></td><td>-</td></tr>
<tr><td><code>on</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">{
   "true": "lightbulb-on",
   "false": "lightbulb-off-outline"
}</pre></td><td>-</td></tr>
<tr><td><code>power</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">{
   "true": "lightbulb-on",
   "false": "lightbulb-off-outline"
}</pre></td><td>-</td></tr>
<tr><td><code>dimmer</code></td><td><pre lang="json">{
   "0": {
      "color": "#999"
   }
}</pre></td><td><pre lang="json">{
   "0": "ausgeschaltet"
}</pre></td><td><code>val => val > 0 ? \ %\ : null</code></td><td><pre lang="json">{
   "0": "lightbulb-off-outline",
   "default": "lightbulb-on"
}</pre></td><td>-</td></tr>
<tr><td><code>level</code></td><td><pre lang="json">{
   "0": {
      "color": "#999"
   }
}</pre></td><td><pre lang="json">{
   "0": "ausgeschaltet"
}</pre></td><td><code>val => val > 0 ? \ %\ : null</code></td><td><pre lang="json">{
   "0": "lightbulb-off-outline",
   "default": "lightbulb-on"
}</pre></td><td>-</td></tr>
<tr><td><code>ct</code></td><td>-</td><td>-</td><td><code>°K</code></td><td><pre lang="json">{
   "default": "thermometer"
}</pre></td><td>-</td></tr>
<tr><td><code>colortemperature</code></td><td>-</td><td>-</td><td><code>°K</code></td><td><pre lang="json">{
   "default": "thermometer"
}</pre></td><td>-</td></tr>
<tr><td><code>hue</code></td><td>-</td><td>-</td><td><code>°</code></td><td><pre lang="json">{
   "default": "palette"
}</pre></td><td>-</td></tr>
<tr><td><code>rgb</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">{
   "default": "palette"
}</pre></td><td>-</td></tr>
<tr><td><code>hsv</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">{
   "default": "palette"
}</pre></td><td>-</td></tr>
<tr><td><code>hex</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">{
   "default": "palette"
}</pre></td><td>-</td></tr>
</table>
<h3>Beispielkonfiguration</h3>
<h4>Adapter deconz</h4>
<ul>
<li><code>power</code>
<ul>
<li>state: <code>.on</code></li>
<li>action: <code>.on</code></li>
</ul>
<li><code>level</code>
<ul>
<li>state: <code>.level</code></li>
<li>action: <code>.level</code></li>
</ul>
<li><code>colorTemperature</code>
<ul>
<li>state: <code>.ct</code></li>
<li>action: <code>.ct</code></li>
</ul>
<li><code>hue</code>
<ul>
<li>state: <code>.hue</code></li>
<li>action: <code>.hue</code></li>
</ul>
</ul>
<h4>Adapter hm-prc</h4>
<h5>hmip-brc2</h5>
<ul>
<li><code>power</code>
<ul>
<li>state: <code>.3.STATE</code></li>
<li>action: <code>.4.STATE</code></li>
</ul>
</ul>
<h5>hmip-bdt</h5>
<ul>
<li><code>level</code>
<ul>
<li>state: <code>.3.LEVEL</code></li>
<li>action: <code>.4.LEVEL</code></li>
</ul>
</ul>
<h5>hm-lc-sw1pbu-fm</h5>
<ul>
<li><code>power</code>
<ul>
<li>state: <code>.1.STATE</code></li>
<li>action: <code>.1.STATE</code></li>
</ul>
</ul>
<h4>Adapter hue-extended</h4>
<ul>
<li><code>power</code>
<ul>
<li>state: <code>.action.on</code></li>
<li>action: <code>.action.on</code></li>
</ul>
<li><code>level</code>
<ul>
<li>state: <code>.action.level</code></li>
<li>action: <code>.action.level</code></li>
</ul>
<li><code>colorTemperature</code>
<ul>
<li>state: <code>.action.colorTemperature</code></li>
<li>action: <code>.action.colorTemperature</code></li>
</ul>
<li><code>hue</code>
<ul>
<li>state: <code>.action.hue</code></li>
<li>action: <code>.action.hue</code></li>
</ul>
</ul>
<h4>Adapter hue</h4>
<ul>
<li><code>power</code>
<ul>
<li>state: <code>.on</code></li>
<li>action: <code>.on</code></li>
</ul>
<li><code>level</code>
<ul>
<li>state: <code>.level</code></li>
<li>action: <code>.level</code></li>
</ul>
<li><code>colorTemperature</code>
<ul>
<li>state: <code>.ct</code></li>
<li>action: <code>.ct</code></li>
</ul>
<li><code>hue</code>
<ul>
<li>state: <code>.hue</code></li>
<li>action: <code>.hue</code></li>
</ul>
</ul>
<h4>Adapter shelly</h4>
<ul>
<li><code>power</code>
<ul>
<li>state: <code>.lights.Switch</code></li>
<li>action: <code>.lights.Switch</code></li>
</ul>
<li><code>level</code>
<ul>
<li>state: <code>.lights.brightness</code></li>
<li>action: <code>.lights.brightness</code></li>
</ul>
</ul>
<h4>Adapter zigbee</h4>
<ul>
<li><code>power</code>
<ul>
<li>state: <code>.state</code></li>
<li>action: <code>.state</code></li>
</ul>
<li><code>level</code>
<ul>
<li>state: <code>.brightness</code></li>
<li>action: <code>.brightness</code></li>
</ul>
<li><code>colorTemperature</code>
<ul>
<li>state: <code>.colortemp</code></li>
<li>action: <code>.colortemp</code></li>
</ul>
<li><code>rgb</code>
<ul>
<li>state: <code>.color</code></li>
<li>action: <code>.color</code></li>
</ul>
</ul>

<h2>Gewerk Ort (<code>location</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"map-marker"</pre></td><td>-</td></tr>
<tr><td><code>position</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"map-marker"</pre></td><td>-</td></tr>
<tr><td><code>presence</code></td><td>-</td><td><pre lang="json">{
   "true": "anwesend",
   "false": "abwesend"
}</pre></td><td>-</td><td><pre lang="json">{
   "true": "map-marker-radius",
   "false": "map-marker-remove-outline"
}</pre></td><td>-</td></tr>
<tr><td><code>users</code></td><td>-</td><td><pre lang="json">{
   "": "niemand anwesend"
}</pre></td><td>-</td><td><pre lang="json">{
   "": "account-group-outline",
   "default": "account-group"
}</pre></td><td>-</td></tr>
</table>

<h2>Gewerk Bewegungs-/Präsenzmelder (<code>motion</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"motion-sensor"</pre></td><td>-</td></tr>
<tr><td><code>motion</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">{
   "true": "motion-sensor",
   "false": "motion-sensor-off"
}</pre></td><td>-</td></tr>
<tr><td><code>presence</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">{
   "true": "motion-sensor",
   "false": "motion-sensor-off"
}</pre></td><td>-</td></tr>
</table>
<h3>Beispielkonfiguration</h3>
<h4>Adapter hm-prc</h4>
<h5>hmip-smi55</h5>
<ul>
<li><code>motion</code>
<ul>
<li>state: <code>.3.MOTION</code></li>
</ul>
<li><code>illumination</code>
<ul>
<li>state: <code>.3.ILLUMINATION</code></li>
</ul>
</ul>
<h5>hmip-smi</h5>
<ul>
<li><code>motion</code>
<ul>
<li>state: <code>.1.MOTION</code></li>
</ul>
<li><code>illumination</code>
<ul>
<li>state: <code>.1.ILLUMINATION</code></li>
</ul>
</ul>
<h5>hmip-smo-a</h5>
<ul>
<li><code>motion</code>
<ul>
<li>state: <code>.1.MOTION</code></li>
</ul>
<li><code>illumination</code>
<ul>
<li>state: <code>.1.ILLUMINATION</code></li>
</ul>
</ul>
<h5>hmip-sam</h5>
<ul>
<li><code>motion</code>
<ul>
<li>state: <code>.1.MOTION</code></li>
</ul>
<li><code>illumination</code>
<ul>
<li>state: <code>.1.ILLUMINATION</code></li>
</ul>
</ul>
<h5>hmip-spi</h5>
<ul>
<li><code>presence</code>
<ul>
<li>state: <code>.1.PRESENCE_DETECTION_STATE</code></li>
</ul>
<li><code>illumination</code>
<ul>
<li>state: <code>.1.ILLUMINATION</code></li>
</ul>
</ul>

<h2>Gewerk Rasenmäher-Roboter (<code>mower</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"robot-mower"</pre></td><td>-</td></tr>
</table>

<h2>Gewerk Sensor (<code>sensor</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"mdi-thermometer"</pre></td><td>-</td></tr>
<tr><td><code>temperature</code></td><td>-</td><td>-</td><td><code>°C</code></td><td><pre lang="json">"mdi-thermometer"</pre></td><td>-</td></tr>
<tr><td><code>humidity</code></td><td>-</td><td>-</td><td><code>%</code></td><td>-</td><td>-</td></tr>
<tr><td><code>illumination</code></td><td>-</td><td>-</td><td><code>lux</code></td><td><pre lang="json">"mdi-brightness-7"</pre></td><td>-</td></tr>
<tr><td><code>pressure</code></td><td>-</td><td>-</td><td><code>hPa</code></td><td><pre lang="json">"mdi-air-purifier"</pre></td><td>-</td></tr>
</table>

<h2>Gewerk Server (<code>server</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"server-network"</pre></td><td>-</td></tr>
<tr><td><code>power</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">{
   "true": "server-network",
   "false": "server-network-off"
}</pre></td><td>-</td></tr>
</table>

<h2>Gewerk Rauchmelder (<code>smoke</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"mdi-smoke-detector"</pre></td><td>-</td></tr>
<tr><td><code>alarm</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">{
   "true": "mdi-alarm-light",
   "false": "mdi-alarm-light-outline"
}</pre></td><td>-</td></tr>
</table>

<h2>Gewerk Steckdose (<code>socket</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"power-socket-eu"</pre></td><td>-</td></tr>
<tr><td><code>consumption</code></td><td>-</td><td>-</td><td><code>W</code></td><td><pre lang="json">{
   "default": "mdi-power-plug-off-outline",
   ">0": "mdi-power-plug"
}</pre></td><td>-</td></tr>
<tr><td><code>meter</code></td><td>-</td><td>-</td><td><code>W</code></td><td><pre lang="json">{
   "default": "mdi-power-plug-off-outline",
   ">0": "mdi-power-plug"
}</pre></td><td>-</td></tr>
</table>
<h3>Beispielkonfiguration</h3>
<h4>Adapter hm-prc</h4>
<h5>hmip-ps</h5>
<ul>
<li><code>power</code>
<ul>
<li>state: <code>.3.STATE</code></li>
</ul>
</ul>
<h5>hmip-psm</h5>
<ul>
<li><code>power</code>
<ul>
<li>state: <code>.3.STATE</code></li>
</ul>
<li><code>meter</code>
<ul>
<li>state: <code>.6.POWER</code></li>
</ul>
</ul>

<h2>Gewerk Lautsprecher (<code>speaker</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"speaker"</pre></td><td>-</td></tr>
</table>

<h2>Gewerk Fernseher (<code>tv</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"television"</pre></td><td>-</td></tr>
<tr><td><code>power</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">{
   "true": "television",
   "false": "television-off"
}</pre></td><td>-</td></tr>
</table>

<h2>Gewerk Benutzer (<code>user</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"account"</pre></td><td>-</td></tr>
<tr><td><code>position</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"map-marker"</pre></td><td>-</td></tr>
<tr><td><code>location</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"account"</pre></td><td>-</td></tr>
<tr><td><code>battery</code></td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td></tr>
</table>

<h2>Gewerk Staubsauger-Roboter (<code>vacuum</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"robot-vacuum"</pre></td><td>-</td></tr>
</table>

<h2>Gewerk Wetter-Station (<code>weather-station</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"weather-partly-snowy-rainy"</pre></td><td>-</td></tr>
<tr><td><code>humidity</code></td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td></tr>
<tr><td><code>wind</code></td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td></tr>
<tr><td><code>temperature</code></td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td></tr>
<tr><td><code>illumination</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"mdi-brightness-7"</pre></td><td>-</td></tr>
<tr><td><code>sunshineduration</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"mdi-weather-sunny"</pre></td><td>-</td></tr>
</table>
<h3>Beispielkonfiguration</h3>
<h4>Adapter hm-prc</h4>
<h5>hmip-stho-a</h5>
<ul>
<li><code>temperature</code>
<ul>
<li>state: <code>.1.ACTUAL_TEMPERATURE</code></li>
</ul>
<li><code>humidity</code>
<ul>
<li>state: <code>.1.HUMIDITY</code></li>
</ul>
</ul>
<h5>hmip-swo-b</h5>
<ul>
<li><code>humidity</code>
<ul>
<li>state: <code>.1.HUMIDITY</code></li>
</ul>
<li><code>wind</code>
<ul>
<li>state: <code>.1.WIND_SPEED</code></li>
</ul>
<li><code>temperature</code>
<ul>
<li>state: <code>.1.ACTUAL_TEMPERATURE</code></li>
</ul>
<li><code>illumination</code>
<ul>
<li>state: <code>.1.ILLUMINATION</code></li>
</ul>
<li><code>sunshineduration</code>
<ul>
<li>state: <code>.1.SUNSHINEDURATION</code></li>
</ul>
</ul>

<h2>Gewerk Fenster (<code>window</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"window-closed-variant"</pre></td><td>-</td></tr>
<tr><td><code>open</code></td><td>-</td><td><pre lang="json">{
   "true": "offen",
   "false": "geschlossen"
}</pre></td><td>-</td><td><pre lang="json">{
   "true": "window-open-variant",
   "false": "window-closed-variant"
}</pre></td><td>-</td></tr>
</table>
<h3>Beispielkonfiguration</h3>
<h4>Adapter hm-prc</h4>
<h5>hmip-swdo</h5>
<ul>
<li><code>open</code>
<ul>
<li>state: <code>.1.STATE</code></li>
<li>display: <code>[object Object]</code></li>
</ul>
</ul>
<h5>hmip-srh</h5>
<ul>
<li><code>open</code>
<ul>
<li>state: <code>.1.STATE</code></li>
<li>display: <code>[object Object]</code></li>
</ul>
</ul>
<h5>hm-sec-sco</h5>
<ul>
<li><code>open</code>
<ul>
<li>state: <code>.1.STATE</code></li>
</ul>
</ul>
<h5>hm-sec-sc-2</h5>
<ul>
<li><code>open</code>
<ul>
<li>state: <code>.1.STATE</code></li>
</ul>
</ul>
<h4>Adapter hmip</h4>
<h5>hmip-swdo</h5>
<ul>
<li><code>open</code>
<ul>
<li>state: <code>.channels.1.windowOpen</code></li>
<li>display: <code>[object Object]</code></li>
</ul>
</ul>

<h2>Gewerk Sonstige (<code>_defaults</code>)</h2>
<h3>vordefinierte Datenpunkte</h3>
<table><tr><th>Datenpunkt Bezeichner</th><th>Datenpunkt Stil</th><th>Anzeige</th><th>Einheit</th><th>Icon</th><th>Icon Stil</th></tr>
<tr><td><code>_any</code></td><td><pre lang="json">{
   "true": {
      "color": "#090",
      "fontWeight": "bold"
   },
   "false": {
      "color": "#999"
   }
}</pre></td><td><pre lang="json">{
   "true": "on",
   "false": "off"
}</pre></td><td>-</td><td>-</td><td>-</td></tr>
<tr><td><code>battery</code></td><td>-</td><td>-</td><td><code>%</code></td><td><pre lang="json">{
   ">80": "battery-high",
   "<=80": "battery-medium",
   "<=30": "battery-low",
   "<=10": "battery-outline",
   "<=5": "battery-alert-variant-outline"
}</pre></td><td>-</td></tr>
<tr><td><code>door</code></td><td>-</td><td><pre lang="json">{
   "true": "open",
   "false": "closed"
}</pre></td><td>-</td><td><pre lang="json">{
   "true": "door-open",
   "false": "door-closed"
}</pre></td><td>-</td></tr>
<tr><td><code>humidity</code></td><td>-</td><td>-</td><td><code>%</code></td><td><pre lang="json">"water-percent"</pre></td><td>-</td></tr>
<tr><td><code>level</code></td><td>-</td><td>-</td><td><code>%</code></td><td>-</td><td>-</td></tr>
<tr><td><code>lowbattery</code></td><td><pre lang="json">{
   "true": {
      "color": "#900",
      "fontWeight": "bold"
   },
   "false": {
      "color": "#999"
   }
}</pre></td><td><pre lang="json">{
   "true": "niedrig",
   "false": "voll"
}</pre></td><td>-</td><td><pre lang="json">{
   "true": "battery-alert-variant-outline",
   "false": "battery-high"
}</pre></td><td>-</td></tr>
<tr><td><code>position</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"map-marker"</pre></td><td>-</td></tr>
<tr><td><code>power</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"power"</pre></td><td>-</td></tr>
<tr><td><code>reachability</code></td><td><pre lang="json">{
   "true": {
      "color": "#090"
   },
   "false": {
      "color": "#900",
      "fontWeight": "bold"
   }
}</pre></td><td><pre lang="json">{
   "true": "erreichbar",
   "false": "nicht erreichbar"
}</pre></td><td>-</td><td><pre lang="json">{
   "true": "lan-connect",
   "false": "lan-disconnect"
}</pre></td><td>-</td></tr>
<tr><td><code>temperature</code></td><td>-</td><td>-</td><td><code>°C</code></td><td><pre lang="json">"thermometer"</pre></td><td>-</td></tr>
<tr><td><code>trigger</code></td><td>-</td><td>-</td><td>-</td><td><pre lang="json">"power"</pre></td><td>-</td></tr>
<tr><td><code>unreach</code></td><td><pre lang="json">{
   "true": {
      "color": "#900",
      "fontWeight": "bold"
   },
   "false": {
      "color": "#090"
   }
}</pre></td><td><pre lang="json">{
   "true": "nicht erreichbar",
   "false": "erreichbar"
}</pre></td><td>-</td><td><pre lang="json">{
   "true": "lan-disconnect",
   "false": "lan-connect"
}</pre></td><td>-</td></tr>
<tr><td><code>wind</code></td><td>-</td><td>-</td><td><code>km/h</code></td><td><pre lang="json">"weather-windy"</pre></td><td>-</td></tr>
</table>
<h3>Beispielkonfiguration</h3>
<h4>Adapter hm-prc</h4>
<h5>hmip-wrc2</h5>
<ul>
<li><code>PRESS_LONG_BOTTOM</code>
<ul>
<li>state: <code>.1.PRESS_LONG</code></li>
<li>action: <code>.1.PRESS_LONG</code></li>
</ul>
<li><code>PRESS_SHORT_BOTTOM</code>
<ul>
<li>state: <code>.1.PRESS_SHORT</code></li>
<li>action: <code>.1.PRESS_SHORT</code></li>
</ul>
<li><code>PRESS_LONG_TOP</code>
<ul>
<li>state: <code>.2.PRESS_LONG</code></li>
<li>action: <code>.2.PRESS_LONG</code></li>
</ul>
<li><code>PRESS_SHORT_TOP</code>
<ul>
<li>state: <code>.2.PRESS_SHORT</code></li>
<li>action: <code>.2.PRESS_SHORT</code></li>
</ul>
</ul>
