DayZ PC Chernarus Files & Code Snippets To Add AI Guarded / Controlled Roadblocks At Several Locations, Mod Changelog & Terms Of Use

MUST BE USED IN CONJUCTION WITH THE EXPANSION AI MOD, WHICH ALREADY MUST BE INSTALLED ON YOUR SERVER.
https://steamcommunity.com/sharedfiles/filedetails/?id=2792982069

Limited Testing on PC Chernarus Local Server DAYZ Version 1.18 July 2022.

MANY THANKS TO THE EXPANSION TEAM FOR CREATING SUCH AN AMAZING MOD.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded xml files could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded xml files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

AS ABOVE, PLEASE ENSURE YOU HAVE EXPANSION AI MOD INSTALLED AND WORKING ON YOUR SERVER BEFORE ADDING THESE ROADBLOCK FILES AND XML SNIPPETS.

To download the required files from this github, click on the green "code" button and then "Download Zip" and extract / unzip on your local drive.

I have included the DayZ Editor compatible "editable-road-blocks-chernarus.dze" file so that you can customise the road-blocks if you wish, then re-export.

1)The roadblocks themselves are spawned in using the custom object spawner json file "road-blocks-chernarus.json"

Ensure the your cfggameply.json file is activated in your online server settings panel, or in your serverDZ.cfg file, in which case you should have
a line like this:
enableCfgGameplayFile = 1;

I recommend your create a folder named "custom" within your mission folder, and then upload "road-blocks-chernarus.json" to that custom folder.

Next edit your cfggameplay.json file object spawner line to look like this:

"objectSpawnersArr": ["custom/road-blocks-chernarus.json"],

If you already are using some custom object spawns, the line will look something like this:

"objectSpawnersArr": ["custom/yourfile.json","custom/anotherfile.json","custom/road-blocks-chernarus.json"],

Remember to Save and re-upload if necessary.

2)You can add the AI that guard the road-blocks in two ways. You can upload the complete "AIPatrolSettings.json" included in this github over the top
of the existing file of the same name which can be found in your mission folder, inside the "expansion" then "settings folder. The catch is with this method is
that this file may well become out of date as the mod is updated.

The best technique is to copy and paste the below code into the existing "AIPatrolSettings.json" file. This way you'll have the latest settings.

Under the entry  "Patrols": [ 

paste the following code:

 {
            "Faction": "Mercenaries",
            "LoadoutFile": "TTSKOLoadout",
            "NumberOfAI": 3,
            "Behaviour": "HALT",
            "Speed": "WALK",
            "UnderThreatSpeed": "WALK",
            "CanBeLooted": 1,
            "UnlimitedReload": 0,
            "MinDistRadius": -2.0,
            "MaxDistRadius": -2.0,
            "DespawnRadius": -2.200000047683716,
            "MinSpreadRadius": 1.0,
            "MaxSpreadRadius": 10.0,
            "Chance": 1.0,
            "RespawnTime": -2.0,
            "Waypoints": [
                [
                    2664.947509765625,
                126.82585144042969,
                3015.818603515625
                ]
            ]
        },
		
		{
            "Faction": "Mercenaries",
            "LoadoutFile": "TTSKOLoadout",
            "NumberOfAI": 3,
            "Behaviour": "HALT",
            "Speed": "WALK",
            "UnderThreatSpeed": "WALK",
            "CanBeLooted": 1,
            "UnlimitedReload": 0,
            "MinDistRadius": -2.0,
            "MaxDistRadius": -2.0,
            "DespawnRadius": -2.200000047683716,
            "MinSpreadRadius": 1.0,
            "MaxSpreadRadius": 10.0,
            "Chance": 1.0,
            "RespawnTime": -2.0,
            "Waypoints": [
                [
                    3844.716064453125,
                234.93653869628907,
                4786.36376953125
                ]
            ]
        },
	
	{
            "Faction": "Mercenaries",
            "LoadoutFile": "TTSKOLoadout",
            "NumberOfAI": 3,
            "Behaviour": "HALT",
            "Speed": "WALK",
            "UnderThreatSpeed": "WALK",
            "CanBeLooted": 1,
            "UnlimitedReload": 0,
            "MinDistRadius": -2.0,
            "MaxDistRadius": -2.0,
            "DespawnRadius": -2.200000047683716,
            "MinSpreadRadius": 1.0,
            "MaxSpreadRadius": 10.0,
            "Chance": 1.0,
            "RespawnTime": -2.0,
            "Waypoints": [
                [
                     10249.591796875,
                26.494564056396486,
                3188.3017578125
                ]
            ]
        },
	
	{
            "Faction": "Mercenaries",
            "LoadoutFile": "TTSKOLoadout",
            "NumberOfAI": 3,
            "Behaviour": "HALT",
            "Speed": "WALK",
            "UnderThreatSpeed": "WALK",
            "CanBeLooted": 1,
            "UnlimitedReload": 0,
            "MinDistRadius": -2.0,
            "MaxDistRadius": -2.0,
            "DespawnRadius": -2.200000047683716,
            "MinSpreadRadius": 1.0,
            "MaxSpreadRadius": 10.0,
            "Chance": 1.0,
            "RespawnTime": -2.0,
            "Waypoints": [
                [
                    10074.37890625,
                257.09033203125,
                8863.6650390625
                ]
            ]
        },
	
	{
            "Faction": "Mercenaries",
            "LoadoutFile": "TTSKOLoadout",
            "NumberOfAI": 3,
            "Behaviour": "HALT",
            "Speed": "WALK",
            "UnderThreatSpeed": "WALK",
            "CanBeLooted": 1,
            "UnlimitedReload": 0,
            "MinDistRadius": -2.0,
            "MaxDistRadius": -2.0,
            "DespawnRadius": -2.200000047683716,
            "MinSpreadRadius": 1.0,
            "MaxSpreadRadius": 10.0,
            "Chance": 1.0,
            "RespawnTime": -2.0,
            "Waypoints": [
                [
                    7095.17724609375,
                255.92236328125,
                6480.31787109375
                ]
            ]
        },
	
	{
            "Faction": "Mercenaries",
            "LoadoutFile": "TTSKOLoadout",
            "NumberOfAI": 3,
            "Behaviour": "HALT",
            "Speed": "WALK",
            "UnderThreatSpeed": "WALK",
            "CanBeLooted": 1,
            "UnlimitedReload": 0,
            "MinDistRadius": -2.0,
            "MaxDistRadius": -2.0,
            "DespawnRadius": -2.200000047683716,
            "MinSpreadRadius": 1.0,
            "MaxSpreadRadius": 10.0,
            "Chance": 1.0,
            "RespawnTime": -2.0,
            "Waypoints": [
                [
                     6633.8271484375,
                139.1641845703125,
                12715.4384765625
                ]
            ]
        },
		
		{
            "Faction": "Mercenaries",
            "LoadoutFile": "TTSKOLoadout",
            "NumberOfAI": 3,
            "Behaviour": "HALT",
            "Speed": "WALK",
            "UnderThreatSpeed": "WALK",
            "CanBeLooted": 1,
            "UnlimitedReload": 0,
            "MinDistRadius": -2.0,
            "MaxDistRadius": -2.0,
            "DespawnRadius": -2.200000047683716,
            "MinSpreadRadius": 1.0,
            "MaxSpreadRadius": 10.0,
            "Chance": 1.0,
            "RespawnTime": -2.0,
            "Waypoints": [
                [
                      2356.59228515625,
                367.9375915527344,
                14129.271484375
                ]
            ]
        },
		
Remember to save and re-upload if necessary.		
		
3) Next, you can optionally add the roadblock items to your mapgrouppos.xml, so that the tents and other props will spawn items as part of the CLE.
This is not necessary to make the roadblocks work, but is a nice touch. If you wish to do this, open your mapgroupos.xml file which is in your mission folder,
and at the top, but below <map> copy and paste the following:

<!--AI Roadblocks Loot-->
	<group name="Land_Mil_Tent_Big2_4" pos="2650.525391 128.947021 3019.903076" rpy="-2.056215 4.166326 0.000000" a="90"/>
	<group name="StaticObj_Misc_Barbedwire" pos="2662.189697 128.137222 3026.686035" rpy="0.761056 4.915711 0.000000" a="90"/>
	<group name="StaticObj_Wall_CncBarrier_4Block" pos="2669.681152 125.833160 2997.997070" rpy="0.531478 6.310594 0.000000" a="90"/>
	<group name="StaticObj_Wall_CncBarrier_4Block" pos="2661.691162 126.781837 3005.879395" rpy="0.911701 5.872274 0.000000" a="90"/>
	<group name="StaticObj_Misc_Barbedwire" pos="2685.718506 128.869644 3017.860840" rpy="-2.102549 6.126332 44.402245" a="45.5978"/>
	<group name="StaticObj_Misc_Table" pos="2656.624512 127.379707 3017.647949" rpy="0.990421 4.170573 0.000000" a="90"/>
	<group name="StaticObj_Garbage_Pile5" pos="2656.330078 124.116997 2990.120117" rpy="-2.870920 8.099800 0.000000" a="90"/>
	<group name="StaticObj_Roadblock_Bags_Curve" pos="3830.421143 236.720154 4785.286133" rpy="2.184372 2.280233 -26.548994" a="116.549"/>
	<group name="StaticObj_Roadblock_Bags_Curve" pos="3857.528809 235.340759 4789.151367" rpy="-2.060555 -1.803366 151.635117" a="-61.6351"/>
	<group name="StaticObj_Roadblock_Bags_Long" pos="3846.352783 235.151611 4779.840332" rpy="-0.205215 2.953789 -75.996719" a="165.997"/>
	<group name="StaticObj_Roadblock_Bags_Long" pos="3843.197021 235.337128 4780.813965" rpy="-0.146043 -2.957279 110.789566" a="-20.7896"/>
	<group name="StaticObj_Roadblock_Bags_Long" pos="3840.164307 235.512695 4782.071777" rpy="0.268826 3.093367 -67.943283" a="157.943"/>
	<group name="StaticObj_Roadblock_Bags_Long" pos="3837.174072 235.687363 4783.273438" rpy="-0.271383 -3.093145 112.103920" a="-22.1039"/>
	<group name="StaticObj_Roadblock_Bags_Long" pos="3841.064941 235.280502 4794.119141" rpy="3.124309 0.988492 -74.488029" a="164.488"/>
	<group name="StaticObj_Roadblock_Bags_Long" pos="3850.437012 235.280502 4791.257813" rpy="-2.952728 -0.919069 107.452019" a="-17.452"/>
	<group name="StaticObj_Roadblock_Bags_Long" pos="3847.228516 235.280502 4792.034180" rpy="-0.098204 -3.208856 105.456459" a="-15.4565"/>
	<group name="StaticObj_Roadblock_Bags_Long" pos="3844.120850 235.280502 4793.103027" rpy="3.124309 0.988492 -74.488029" a="164.488"/>
	<group name="StaticObj_Roadblock_Bags_Curve" pos="3834.573730 236.480469 4795.756348" rpy="2.338686 -2.329703 63.814247" a="26.1858"/>
	<group name="StaticObj_Roadblock_Bags_Curve" pos="3855.645752 235.284576 4778.600098" rpy="-2.450584 1.224825 -140.531891" a="-129.468"/>
	<group name="StaticObj_Misc_Barbedwire" pos="3822.994385 236.763596 4791.160645" rpy="0.009470 3.081764 -69.599792" a="159.6"/>
	<group name="StaticObj_Misc_Barbedwire" pos="3819.370850 237.190506 4799.006836" rpy="-0.024076 -3.010964 111.182014" a="-21.182"/>
	<group name="StaticObj_Misc_Barbedwire" pos="3872.057373 234.249924 4776.603027" rpy="0.005977 -2.496054 102.200447" a="-12.2004"/>
	<group name="StaticObj_Misc_Barbedwire" pos="3866.496338 234.561050 4784.152344" rpy="-0.202960 2.562183 -82.546799" a="172.547"/>
	<group name="Land_Roadblock_WoodenCrate" pos="3843.449951 235.220001 4791.020020" rpy="0.228047 -3.207359 99.645386" a="-9.64539"/>
	<group name="Land_Roadblock_Table" pos="3845.776123 235.249069 4790.392090" rpy="3.128688 0.761134 0.000000" a="90"/>
	<group name="Land_Roadblock_Table" pos="3848.230469 235.112732 4789.937500" rpy="2.824014 0.761625 0.000000" a="90"/>
	<group name="Land_Roadblock_WoodenCrate" pos="3841.040039 235.429001 4791.990234" rpy="0.908952 3.084829 -59.889889" a="149.89"/>
	<group name="Land_Roadblock_WoodenCrate" pos="3850.629883 234.862000 4789.839844" rpy="-0.756100 -2.822440 120.109993" a="-30.11"/>
	<group name="StaticObj_Roadblock_Pillbox" pos="10242.145508 26.706644 3178.037842" rpy="3.601495 -0.406263 126.796310" a="-36.7963"/>
	<group name="StaticObj_Roadblock_Pillbox" pos="10256.720703 28.231676 3199.299805" rpy="-6.925815 0.344526 -42.568436" a="132.568"/>
	<group name="StaticObj_Roadblock_CncBlocks_Long" pos="10232.396484 25.733454 3168.346924" rpy="0.786710 0.332356 130.529068" a="-40.5291"/>
	<group name="StaticObj_Roadblock_CncBlocks_Long" pos="10231.200195 25.570900 3157.570068" rpy="-0.101688 -0.036501 -64.745689" a="154.746"/>
	<group name="StaticObj_Roadblock_CncBlocks_short" pos="10262.099609 29.049801 3212.020020" rpy="5.547190 -1.543269 129.766983" a="-39.767"/>
	<group name="StaticObj_Roadblock_CncBlocks_short" pos="10272.000000 30.593100 3219.899902" rpy="9.767610 -3.047550 133.231964" a="-43.232"/>
	<group name="StaticObj_Misc_Barbedwire" pos="10244.601563 27.203615 3204.680664" rpy="-4.952899 0.681436 0.000000" a="90"/>
	<group name="Land_Mil_Tent_Big2_4" pos="10077.099609 259.330994 8854.809570" rpy="7.154121 -5.199448 -10.003598" a="100.004"/>
	<group name="StaticObj_Mil_HBarrier_6m" pos="10052.789063 260.620331 8853.260742" rpy="1.277225 7.339005 -108.373932" a="-161.626"/>
	<group name="StaticObj_Mil_HBarrier_6m" pos="10060.842773 259.391785 8861.778320" rpy="-2.331809 -7.773827 83.023796" a="6.9762"/>
	<group name="StaticObj_Mil_HBarrier_6m" pos="10100.569336 255.496796 8869.045898" rpy="1.745150 6.227091 -113.371582" a="-156.628"/>
	<group name="StaticObj_Mil_HBarrier_6m" pos="10108.105469 254.007904 8877.154297" rpy="2.385288 7.449436 -107.410927" a="-162.589"/>
	<group name="StaticObj_Misc_Barbedwire" pos="10058.627930 260.636993 8846.274414" rpy="3.875280 -7.710651 19.450512" a="70.5495"/>
	<group name="StaticObj_Misc_Barbedwire" pos="10067.196289 260.280182 8845.431641" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Misc_Barbedwire" pos="10025.540039 263.793671 8857.773438" rpy="0.041258 -7.993579 43.202667" a="46.7973"/>
	<group name="StaticObj_Misc_Barbedwire" pos="10112.460938 252.708221 8884.562500" rpy="-9.974623 2.126154 141.275345" a="-51.2753"/>
	<group name="StaticObj_Misc_Barbedwire" pos="10082.229492 257.079041 8876.817383" rpy="-2.889235 -2.647726 166.452011" a="-76.452"/>
	<group name="StaticObj_Misc_Barbedwire" pos="10070.740234 258.024109 8873.228516" rpy="9.381078 -3.837790 -18.696203" a="108.696"/>
	<group name="StaticObj_Misc_Barbedwire" pos="7089.204102 256.249268 6498.490723" rpy="-0.076468 0.229169 0.000000" a="90"/>
	<group name="StaticObj_Misc_Barbedwire" pos="7097.484375 256.391327 6488.387207" rpy="-0.152678 -1.069075 0.000000" a="90"/>
	<group name="StaticObj_Misc_Barbedwire" pos="7104.454590 257.258179 6466.932617" rpy="0.045140 -1.913028 -24.849543" a="114.85"/>
	<group name="StaticObj_Misc_Barbedwire" pos="7095.565430 257.044067 6470.404785" rpy="0.107490 -2.051102 -24.799944" a="114.8"/>
	<group name="Land_Shed_M3" pos="7086.279785 257.186005 6482.819824" rpy="7.442080 -1.434330 0.000000" a="90"/>
	<group name="Land_Shed_W5" pos="7085.589844 257.375000 6488.339844" rpy="-8.890358 1.214250 -177.045959" a="-92.954"/>
	<group name="StaticObj_Furniture_foldingbed_open" pos="7084.700195 256.029999 6487.450195" rpy="1.593430 7.347919 -88.805382" a="178.805"/>
	<group name="StaticObj_Furniture_foldingbed_open" pos="7084.529785 256.029999 6489.180176" rpy="1.280280 7.317707 -86.534782" a="176.535"/>
	<group name="Land_Roadblock_Table" pos="7100.127930 256.304016 6480.014648" rpy="1.886078 -0.002037 -111.308289" a="-158.692"/>
	<group name="Land_Roadblock_Table" pos="7101.173828 256.409058 6477.842773" rpy="-2.518390 -0.312368 67.214134" a="22.7859"/>
	<group name="Land_Roadblock_Table" pos="7100.120117 256.229828 6482.419922" rpy="-0.152582 -2.287569 0.000000" a="90"/>
	<group name="Land_Roadblock_WoodenCrate" pos="7102.120117 256.354004 6475.529785" rpy="-0.806312 -2.403970 2.822780" a="87.1772"/>
	<group name="Land_Roadblock_WoodenCrate" pos="7103.810059 256.466003 6473.520020" rpy="-0.008986 -2.606249 -20.358299" a="110.358"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6609.916016 139.548859 12720.948242" rpy="1.603908 -0.152720 0.000000" a="90"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6602.877930 140.009094 12719.436523" rpy="4.570034 -2.050469 0.024141" a="89.9759"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6597.147461 140.575562 12717.615234" rpy="4.731666 -2.858676 -0.236152" a="90.2362"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6618.145996 139.394730 12724.070313" rpy="0.458340 0.152802 0.001222" a="89.9988"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6622.668457 139.349045 12721.494141" rpy="-0.000000 0.000000 0.001222" a="89.9988"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6627.107422 139.354050 12718.739258" rpy="-0.000000 -0.229169 0.000000" a="90"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6661.302246 138.250015 12701.489258" rpy="0.611316 0.890392 26.334639" a="63.6654"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6656.623535 138.482635 12704.119141" rpy="-3.190078 0.530355 -151.255646" a="-118.744"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6652.929199 138.694061 12704.887695" rpy="-3.045891 1.084657 -141.078690" a="-128.921"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6645.723145 139.109146 12703.258789" rpy="-4.089575 1.030447 -153.291885" a="-116.708"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6643.665039 139.257095 12707.248047" rpy="-1.422498 -0.524012 -151.139664" a="-118.86"/>
	<group name="StaticObj_Roadblock_CncBlock" pos="6640.697754 139.380249 12710.833984" rpy="1.460375 0.406819 33.518009" a="56.482"/>
	<group name="StaticObj_Misc_Barbedwire" pos="6654.446777 138.983398 12692.754883" rpy="2.758998 3.192525 -74.898872" a="164.899"/>
	<group name="StaticObj_Misc_Barbedwire" pos="6649.081055 139.418655 12690.605469" rpy="2.514038 3.110249 -72.327721" a="162.328"/>
	<group name="StaticObj_Misc_Barbedwire" pos="6666.961426 139.152847 12706.291992" rpy="14.245568 -2.466202 131.603210" a="-41.6032"/>
	<group name="StaticObj_Misc_Barbedwire" pos="6594.911133 141.388443 12712.180664" rpy="1.171199 4.173151 -59.116241" a="149.116"/>
	<group name="StaticObj_Misc_Barbedwire" pos="6596.228516 141.218033 12732.662109" rpy="-4.518893 1.425905 -117.422295" a="-152.578"/>
	<group name="StaticObj_Misc_Barbedwire" pos="6590.564453 141.929169 12738.572266" rpy="-5.747067 0.493541 -107.569252" a="-162.431"/>
	<group name="StaticObj_Misc_Barbedwire" pos="6583.662598 143.087830 12746.250977" rpy="-3.816079 1.701631 -117.576302" a="-152.424"/>
	<group name="Land_Mil_Fortified_Nest_Watchtower" pos="6603.396973 142.033661 12711.777344" rpy="-1.733698 -5.297170 93.089386" a="-3.08939"/>
	<group name="Land_Mil_Fortified_Nest_Watchtower" pos="6640.463379 141.266937 12696.669922" rpy="3.030517 2.927336 -64.169830" a="154.17"/>
	<group name="Land_Mil_Tent_Big2_4" pos="2363.349365 369.606079 14132.338867" rpy="0.451690 -1.299832 67.662727" a="22.3373"/>
	<group name="StaticObj_Roadblock_Bags_Curve" pos="2359.175781 369.013611 14140.927734" rpy="3.473659 -5.959559 57.493912" a="32.5061"/>
	<group name="StaticObj_Roadblock_Bags_Curve" pos="2364.503418 368.935577 14121.272461" rpy="4.491052 1.600745 -96.757141" a="-173.243"/>
	<group name="StaticObj_Misc_Barbedwire" pos="2377.767090 365.677979 14139.665039" rpy="-1.865720 13.997091 -126.878998" a="-143.121"/>
	<group name="StaticObj_Misc_Barbedwire" pos="2375.076416 367.178925 14131.856445" rpy="-6.116516 -8.999174 116.166992" a="-26.167"/>
	<group name="StaticObj_Misc_Barbedwire" pos="2341.417725 372.070679 14156.288086" rpy="-0.358343 8.434002 -57.445694" a="147.446"/>
	<group name="StaticObj_Misc_Barbedwire" pos="2365.491211 370.357788 14103.907227" rpy="-0.836553 -5.432292 0.000000" a="90"/>
	<!--End AI Roadblocks Loot-->

Remember to save and re-upload if necessary.

4) Restart your server and the AI guarded Road Blocks should spawn in.

Thanks, Rob.