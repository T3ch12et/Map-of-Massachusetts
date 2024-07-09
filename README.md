# Map of Massachusetts
A reference map depicting the state of Massachusetts, capturing its geographical and key administrative features in a compact format.

<img src="./MapOfMassachusetts.png" img alt = "Massachusetts Map"/>

## How It's Made:

**Tech used:** ArcGIS Pro

I began by downloading the Massachusetts dataset and selecting the "Counties_northeast" layer, which I moved to the bottom of the Contents pane. My goal was to highlight Massachusetts distinctly. Opening the Symbology pane from the Feature Layer tab, I chose "Unique Values" to differentiate the state names. From Field 1, I selected STATE_NAME, removed all states except Massachusetts, and assigned a unique symbol to highlight it. This made Massachusetts stand out with a distinctive color, while the other states were represented by a default symbol.

Next, I modified the symbology of the states surrounding Massachusetts. In the Symbology pane, I clicked the Format Symbol color swatch next to "All Other Values," which opened the Format Polygon Symbol pane. This pane has two primary tabs: Gallery and Properties. The Gallery offers existing symbols, while the Properties tab provides control over the symbol's appearance. In the Properties tab, under the Symbol section, I selected Color and went to Color Properties. Because this map was intended for hard-copy printing, I changed the color model to CMYK, which is ideal for subtractive color output. I set the values to Cyan = 10%, Magenta = 10%, Yellow = 20%, and Black = 5%, saved this style as "States," and set the Outline Color to "No Color" with an Outline Width of 0 pt. Now, all states except Massachusetts were a solid green color without visible lines.

For Massachusetts, I created a custom color style by setting the CMYK values to Cyan = 5%, Magenta = 5%, Yellow = 15%, and Black = 0%. This lighter green color was saved as "Massachusetts," ensuring it remained the focal point. Light background colors support detailed features, enhancing visual hierarchy and contrast on the map.

I then worked on the UrbanArea_MA layer, placing it second from the bottom. I zoomed to this layer, selected its symbol, and applied a 50% transparency to the "States" color, subtly implying urban areas without overpowering other features. The Outline Color and Width were also set to "No Color" and 0 pt, respectively.

For the Parks_MA layer, I differentiated types of public parks using data attributes. Moving this layer above UrbanAreas_MA, I applied "Unique Values" based on the FEATTYPE attribute. National Parks or Forests were assigned CMYK values of 40% Cyan, 20% Magenta, 50% Yellow, and 10% Black with no outline, saved as "National." State Parks or Forests were given CMYK values of 30% Cyan, 15% Magenta, 35% Yellow, and 5% Black with no outline, saved as "State." Local and Regional Parks were excluded, and I unchecked "Show All Other Values" in the Symbology pane.

Next, I symbolized line features for different highway types in the Highways_MA layer. Placing it above the Public Lands layer, I used "Unique Values" in the Symbology pane with the HwyClass field, showing four highway types. Utilizing the symbol gallery, I assigned a thick orange "Highway" symbol to Interstate Highways and a lighter, thinner "Major Road" symbol to State and US Highways. Major Roads were symbolized with a "Minor Road" symbol.

To ensure the highways and roads looked appropriately scaled, I set a map reference scale of 1:1,000,000, making symbols constant in size relative to geography. This adjustment made the symbols proportionate and visually connected.

Finally, I enabled the Maplex Label Engine for advanced label placement. Using the Places_MA layer, I placed city names without point symbols. To avoid clutter, I filtered cities with a population of at least 15,000 using a definition query. This reduced the labels to 51 cities, enhancing readability.

Adjusting label placement, I selected "Best Position" and enabled "Stack Label" under the Fitting Strategy tab. I set the font to a dark gray to reduce contrast and applied these settings. The final step was to set the Color and Outline of the Places_MA layer to "No Color," ensuring labels didn't overlap with other map features.

This project not only highlighted Massachusetts effectively but also demonstrated my ability to manage complex symbology, data attributes, and label placement, ensuring a clear, visually appealing, and accurate map.

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
