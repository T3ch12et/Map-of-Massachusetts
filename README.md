# Map of Massachusetts
A reference map depicting the state of Massachusetts, capturing its geographical and key administrative features in a compact format.

<img src="./MapOfMassachusetts.png" img alt = "Massachusetts Map"/>

## How It's Made:

**Tech used:** ArcGIS Pro

I downloaded the dataset of Masachusetts data and selected the Counties_norteast layer that was mvoed to the bottom of the Contents pane then opened the Symbology pane from the Feature Layer tab. The goal is to showcase one feature in the map, which the state of Massachusetts. In the Symbology pane I selected the Unique Values which shows the different values regarding the different state names. From Field 1 I chose STATE_NAME and selected every state except Massachusetts and removed them. Massachusetts is now highlighted with a unique symbol to distinguish it from the other states, which are all drawn with the symbol defined for "all other values."

Now it's time to modify the symbology of the states surrounding Massachusetts. In the Symbology pane, next to All Other Values, I clicked the Format Symbol color swatch which opens the Format Polygon Symbol pane used to change symbols as they are applied to features. The pane has two primary tabs: Gallery giving me access to a gallery of existing symbols I can choose from and Properties tab giving me access to all the properties of the current symbol giving me control over the symbol's appearance. I opened the Properties tab and within that tab selected teh Symbol tab. In teh Appearance section I selected Color and went to Color Properties. Because you are making a map for hard-copy printing, you will change the color model to CMYK. CMYK is a subtractive color model that relates to subtractive output. Printing colored ink, usually in Cyan, Magenta, Yellow, or blacK, subtracts from the white light reflected from the page. This contrasts with an additive color model like RGB, where the Red, Green, and Blue light from within your monitor add together to change your dark monitor to bright white. I set teh Color Mode to CMYK and set the values to: Cyan = 10%, Magenta = 10%, Yellow = 20%, Black = 5%. From there I saved the color style and named it States. After accepting the options, in teh Format Symbol pane, I set the Outline Color to "No Color" and set the Outline Width to 0pt. Now all states except Massachusetss is a solid green color with no lines visible.

Next up is to create a custom color style for Massachusetts. This time I went to Format Polygon Symbol pane for Massachusetts and went to Color Properties to fill in the CMYK with the following values: Cyan = 5%, Magenta = 5%, Yellow = 15%, Black = 0%. I saved this color style as Massachusetts and did the same steps for the Outline Color and Outline WIdth being set to "No Color" and 0pt respectively. Now Massachusetts is set at a lighter green color. Using light colors for background information better supports the more detailed features that will appear on the background. The two colors used in your current map are similar, but a brighter version is used to make Massachusetts the focal point. Visual hierarchy is needed for the proper presentation of features on the map that implies relative importance and achieved through visual contrast. I put the UrbanArea_MA layer so that it's second to the bottom. I zoomed to the layer and selected the color symbol below the layer name in the Contents pane. I selected the States colors and went on Color Properties to put 50% transparency to lighten it. The urban areas are subtly implied with a darker fill but still will not overpower or interfere with features that appear above them. The Outline Color and Outline Width are set to "No Color" and 0 pt respectively.

For the Parks_MA layer, I have to use data attributes to differentiate types of public parks. I moved the layer above the UrbanAreas_MA layer and used Unique Values and the FEATTYPE attribute value for each type of park. Make National Park Or Forest CMYK 40% 20% 50% 10% with no outline, and save the color to your favorites as National. Make State Park Or Forest CMYK 30% 15% 35% 5% with no outline, and save the color to your favorites as State and did not include Local Park or Regional Park. After that is all said and done I unchecked the Show All Other Values box in the Symbology pane. 

Next up is to used the symbol gallery to symbolize line features of differenrr types of highways in the Highways_MA layer. I moved it above the Public Lands layer, previosuly named Parks_MA layer, and went into the Symbology pane for the Highways_MA layer and selected Unique Values for it. For the Field 1 selection, the HwyClass field was selected to show the four different highway types. To streamline the process of modifying symboles, I used the symbols available in the symbol gallery. I selected the symbol for Interstate Highways and from the Format Line Symbol pane I clicked the Gallery tab and clicked on the "Highway" symbol, it was a thick orange line. Then I did the same thing for the State Highways and US Highways layers and chose the "Major Road" symbol which is half the thickness of teh "Highway" symbol and it's a light orange color. I then symbolized the Major Roads with the "Minor Road" symbol. 

Even though all roads have been symbolized, the roads and highways look overly thick or too thin since there is no reference scale set. 

## Lessons Learned:

No matter what your experience level, being an engineer means continuously learning. Every time you build something you always have those *whoa this is awesome* or *wow I actually did it!* moments. This is where you should share those moments! Recruiters and interviewers love to see that you're self-aware and passionate about growing.

## Repositories
**Profile:** [T3ch12et](https://github.com/T3ch12et)

**Cartography Repository:** [ESRI MOOC Cartography](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography)

**Main Repository:** [GIS Data Science Portfolio](https://github.com/T3ch12et/GIS-Data-Science-Portfolio)

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Palettable:** https://github.com/alecortega/palettable

**Twitter Battle:** https://github.com/alecortega/twitter-battle

**Patch Panel:** https://github.com/alecortega/patch-panel
