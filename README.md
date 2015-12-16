# HighlightMarker
HighlightMarker is a library which supports you in highlighting an input string in a given text. Essentially, it tells you from/to which character of a given text you need to start/stop highlighting the user's search input.

### Download and Install HighlightMarker
This library is available on NuGet: https://www.nuget.org/packages/HighlightMarker/
Use the following command to install HighlightMarker using NuGet package manager console:

    PM> Install-Package HighlightMarker

You can use this library in any .Net project which is compatible to PCL (e.g. Xamarin Android, iOS, Windows Phone, Windows Store, Universal Apps, etc.). There is a special NuGet package for Xamarin.Forms available:

    PM> Install-Package HighlightMarker.Forms

### How to use HighlightMarker
#### Using HighlightMarker in Xamarin.Forms
In the folder Samples\HighlightMarker.Forms you can find a Xamarin.Forms demo project which displays a searchable list of shopping malls. The ```<ViewCell.View>``` defines a custom cell template for the malls list. The most interesting part are the custom bindings named ```TextHighlightBehavior.HighlightedText``` and ```TextHighlightBehavior.FullText```. All you need to do is binding the HighlightedText property to the search string (in our case we reference the Text property of the SearchBar) and binding the FullText property to the ViewModel property. 

```
    <Label forms:TextHighlightBehavior.HighlightedText="{Binding Text, Source={x:Reference SearchBar}}"
           forms:TextHighlightBehavior.FullText="{Binding Title}" />
```

#### Using HighlightMarker in Xamarin.Android projects
TODO: Document usage of ```TextViewExtensions```.

#### Using HighlightMarker in Xamarin.iOS projects
TODO: Document usage of ```UILabelExtensions```.

#### Using HighlightMarker in Windows Phone projects
TODO: Document usage of ```SearchTextHighlighting``` and its attached dependency properties.

#### Using HighlightMarker in any C# project
To explain the usage of HighlightMarker, it's best to consult the existing unit tests. Following test shows how a certain ```FullText``` is highlighted with the string ```SearchText```:

```
// Arrange
const string FullText = "full text for highlight marking";
const string SearchText = "highlight";
var highlightMarker = new HighlightMarker(FullText, SearchText);

// Act
var highlightList = highlightMarker.ToList();

// Assert
```
![GitHub Logo](/readme/images/highlightlist.png)

### License
HighlightMarker is Copyright &copy; 2015 [Thomas Galliker](https://ch.linkedin.com/in/thomasgalliker). Free for non-commercial use. For commercial use please contact the author.


### Sources

https://developer.xamarin.com/recipes/ios/standard_controls/text_field/style_text/

https://www.syntaxismyui.com/xamarin-forms-searchbar-recipe/

https://developer.xamarin.com/guides/cross-platform/xamarin-forms/user-interface/listview/customizing-cell-appearance/#Custom_Cells




