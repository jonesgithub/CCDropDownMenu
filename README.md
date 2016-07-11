## CCDropDownMenu

[![](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/Cokile/CCActivityIndicatorView/blob/master/Licence)
[![](https://img.shields.io/github/release/Cokile/CCDropDownMenu.svg)](https://github.com/Cokile/CCDropDownMenu/releases)

`CCDropDownMenu` now features

|                   Type                   |
| :--------------------------------------: |
| [ManaDropDownMenu](https://github.com/Cokile/CCDropDownMenu#manadropdownmenu) |
| [SyuDropDownMenu](https://github.com/Cokile/CCDropDownMenu#syudropdownmenu) |



## Installation

### Use Cocoapods

Simply add one line to your Podfile:

```ruby
pod 'CCDropDownMenu'
```

### Manually 

Add all the files in the `CCDropDownMenu` folder to your project.



## ManaDropDownMenu

<img src=Captures/capture1.gif width=210 height=372>

### Easy to use

```objective-c
// Note the header name is CCDropDownMenus.h not CCDropDownMenu.h
#import "CCDropDownMenus.h"

// ...
@interface ViewController () <CCDropDownMenuDelegate>

// ...
- (void)viewDidLoad {
	// ...
    ManaDropDownMenu *menu = [[ManaDropDownMenu alloc] initWithFrame:<#CGRect#> 	title:<#NSString#>];
	menu.delegate = self;
    menu.numberOfRows = <#NSInteger#>;
    menu.textOfRows = @[<#NSString#>, <#NSString#>, <#NSString#>, ...];
  	[self.view addSubview:menu];
}

- (void)dropDownMenu:(CCDropDownMenu *)dropDownMenu didSelectRowAtIndex:(NSInteger)index {
  	// ...
}
```

### Customisable

```objective-c
// The color that applys to the title and the arrow when the drop down menu is expanded. Default value is a orange color.
menu.activeColor = <#UIColor#>;

// The color that applys to the title and the arrow when the drop down menu is closed. Default value is a gray color.
menu.inactiveColor = <#UIColor#>;

// The color that applys to the seperator for the title and the indicator. Default value is a gray color.
menu.seperatorColor = <#UIColor#>;

// The color that applys to the title view. Default value is a white color.
menu.titleViewColor = <#UIColor#>;

// The string that applys to the title for the drop down menu.
menu.title = <#NSString#>;

// The image that applys to the right indicator for the drop down menu. Default value is a arrow image.
menu.indicator = <#UIImage#>;

// The value that applys to the gutter distance between list view. Default value is 0.
menu.gutter = <#CGFloat#>;

// The boolean value that indicates the weahter apply a resilient when expansion. Default value is NO.
menu.resilient = <#BOOL#>;

// The value that applys to the height for row of the drop down menu.
menu.heightOfRows = <#CGFloat#>;
  	
// The strings that represent the name of the image for each row.
menu.imageNameOfRows = @[<#NSString#>, @<#NSString#>, <#NSString#>, ...];
  
// The colors that applys to background color for each row.   
menu.colorOfRows = @[<#UIColor#>, <#UIColor#>, <#UIColor#>, ...];
```



## SyuDropDownMenu

![](Captures/capture2.gif)

### Easy to use

```objective-c
// Note the header name is CCDropDownMenus.h not CCDropDownMenu.h
#import "CCDropDownMenus.h"

// ...
@interface ViewController () <CCDropDownMenuDelegate>

// ...
- (void)viewDidLoad {
	// ...
  	// You should set the batTintColor of the navigation first.
    SyuDropDownMenu *menu = [[SyuDropDownMenu alloc] initWithNavigationBar:<#UINavigationBar#> useNavigationController:<#BOOL#>;
	menu.delegate = self;
    menu.numberOfRows = <#NSInteger#>;
  	[self.view addSubview:menu];
}

- (void)dropDownMenu:(CCDropDownMenu *)dropDownMenu didSelectRowAtIndex:(NSInteger)index {
  	// ...
}
```

### Customisable

```objective-c
// The color that applys to the title and the arrow when the drop down menu is expanded. Default value is a light blue color.
menu.activeColor = <#UIColor#>;

// The color that applys to the title and the arrow when the drop down menu is closed. Default value is a gray color.
menu.inactiveColor = <#UIColor#>;

// The color that applys to the title view. Default value is the bar tint color of the navigation bar.
menu.titleViewColor = <#UIColor#>;

// The image that applys to the right indicator for the drop down menu. Default value is a arrow image.
menu.indicator = <#UIImage#>;

// The value that applys to the gutter distance between list view. Default value is 0.
menu.gutter = <#CGFloat#>;

// The boolean value that indicates the weahter apply a resilient when expansion. Default value is NO.
menu.resilient = <#BOOL#>;

// The value that applys to the height for row of the drop down menu.
menu.heightOfRows = <#CGFloat#>;
  
// The colors that applys to background color for each row.   
menu.colorOfRows = @[<#UIColor#>, <#UIColor#>, <#UIColor#>, ...];
```



## Requirement

CCDropDownMenu requires ARC.



## TODO

- More types of drop down menu.
- Performance improvement



Any Pull Requests and issues are welcome. 