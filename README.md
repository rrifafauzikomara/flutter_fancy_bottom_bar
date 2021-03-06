# FancyBottomNavigation

[pub package](https://pub.dev/packages/fancy_bottom_navigation)

A Flutter package for easy implementation of fancy bottom navigation. 

![Fancy Gif](https://github.com/rrifafauzikomara/flutter_fancy_bottom_bar/blob/master/fancy_gif.gif "Fancy Gif")

<img src="fancy.png" width="250" height="444">

## Add dependency

```yaml
dependencies:
  ...
  fancy_bottom_navigation: ^0.3.2
```

## Limitations
For now this is limited to more than 1 tab, and less than 5. So 2-4 tabs.

## Basic Usage

Adding the widget
```dart
bottomNavigationBar: FancyBottomNavigation(
    tabs: [
        TabData(iconData: Icons.home, title: "Home"),
        TabData(iconData: Icons.search, title: "Search"),
        TabData(iconData: Icons.shopping_cart, title: "Basket")
    ],
    onTabChangedListener: (position) {
        setState(() {
        currentPage = position;
        });
    },
)
```

## TabData
**iconData** -> Icon to be used for the tab<br/>
**title** -> String to be used for the tab<br/>
**onClick** -> Optional function to be used when the circle itself is clicked, on an active tab

## Attributes
### required
**tabs** -> List of `TabData` objects<br/>
**onTabChangedListener** -> Function to handle a tap on a tab, receives `int position`

### optional
**initialSelection** -> Defaults to 0<br/>
**circleColor** -> Defaults to null, derives from `Theme`<br/>
**activeIconColor** -> Defaults to null, derives from `Theme`<br/>
**inactiveIconColor** -> Defaults to null, derives from `Theme`<br/>
**taxtColor** -> Defaults to null, derives from `Theme`<br/>
**barBackgroundColor** -> Defaults to null, derives from `Theme`<br/>
**key** -> Defaults to null<br/>

## Theming

The bar will attempt to use your current theme out of the box, however you may want to theme it. Here are the attributes:


![Fancy Theming](https://github.com/rrifafauzikomara/flutter_fancy_bottom_bar/blob/master/fancy_theming.png "Fancy Theming")

## Programmatic Selection

To select a tab programmatically you will need to assign a GlobalKey to the widget. When you want to change tabs you will need to access the State using this key, and then call `setPage(position)`.<br/>
See example project, main.dart, line 75 for an example.

## Author

* **R Rifa Fauzi Komara**

Don't forget to follow and ★
