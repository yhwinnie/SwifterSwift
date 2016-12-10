---
layout: default
---
# v1.3

This version adds **more than 90 new extensions** making it the widest extensions library available online for Swift 3 with **more than 360 properties and methods for more than 35 type**.
This is the biggest update since library launch! we're so excited 🤓

Here are some changes:
- Updated some properties and methods names to follow [Swift API Design Guidelines](//developer.apple.com/videos/play/wwdc2016/403/).
- Added default values to methods parameters (where possible).
- All units documentation has been re-written in xcode,
  - Now you see "**SwifterSwift:** " at the beginning of description to know the source of the extension while writing your code.
  - All method parameters and return types has been documented in xcode as well.
  - All extensions documentation has been re-written in [Wiki](//github.com/omaralbeik/SwifterSwift/wiki), separating properties from methods in different tables.
- All extensions files re-organized in separate extensions based on type (properties, methods, initializers, ..)
- Fixed some bugs where some extensions were not public.
- New section explaining how to add new extensions in [Contributing Guidelines](//github.com/omaralbeik/SwifterSwift/blob/master/CONTRIBUTING.md)
- And finally: new logo

## v1.2.2

###New Extensions:
 - **UIColorExtensions**:
 	- **struct material**: get [Google material palette colors](//material.google.com/style/color.html) with ease

###Updated Extensions:
 - **UIColorExtensions**:
 	- struct socialColors -> **struct social**


## v1.2.1

###New Extensions:

 - **ConvenienceExtensions**:
 	- **func string(forKey: String)**: Get a string from UserDefaults
 	- **func integer(forKey: String)**: Get an integer from UserDefaults
 	- **func double(forKey: String)**: Get a double from UserDefaults
 	- **func float(forKey: String)**: Get a float from UserDefaults
 	- **func data(forKey: String)**: Get a data from UserDefaults
 	- **func bool(forKey: String)**: Get a bool from UserDefaults
 	- **func array(forKey: String)**: Get an array from UserDefaults
 	- **func dictionary(forKey: String)**: Get a dictionary from UserDefaults

 - **StringExtensions**:
 	- **func toDate(withFormat format: String)**: Return Date value from string of date format (if applicable).
 	- **var toURL**: Return URL from string (if applicable).

 - **UIAlertControllerExtensions**:
 	- **addAction(title, style, isEnabled, handler)**: Add an action to Alert.
 	- **addTextField(text, placeholder, editingChangedTarget, editingChangedSelector)**: Add a text field to Alert.

 - **UINavigationBarExtensions**:
 	- **func setColors(background, text)**: Set Navigation Bar background and text colors.


###Updated Extensions:

 - **ConvenienceExtensions**:
 	- var deviceHeight -> **var screenHeight**
 	- var deviceWidth -> **var screenWidth**

 - **ArrayExtensions**:
 	- func removeAll(item: Element) -> **func removeAll(_ item: Element))**

 - **DateExtensions**:
 	- func add(component: Calendar.Component, value: Int) -> **add(_ component: Calendar.Component, value: Int)**
 	- func adding(component: Calendar.Component, value: Int) -> **adding(_ component: Calendar.Component, value: Int)**
 	- func changing(component: Calendar.Component, value: Int) -> **changing(_ component: Calendar.Component, value: Int)**
 	- func isIn(current: Calendar.Component) -> **isInCurrent(_ component: Calendar.Component)**

 - **StringExtensions**:
 	- func contain(string: String, caseSensitive: Bool) -> **func contain(_ string: String, caseSensitive: Bool)**
 	- func lines() -> **var lines**
 	- static func random(of length: Int) -> **static func random(ofLength: Int)**
 	- func replace(string: String, with: String) -> **func replace(_ substring: String, with: String)**
 	- func truncate(to length: Int, trailing: String?) -> **func truncate(toLength: Int, trailing: String?)**
 	- func truncated(to length: Int, trailing: String? = "...") -> **func truncated(to length: Int, trailing: String?)**

 - **UIButtonExtensions**:
 	- func imageForAllStates(image: UIImage) -> **func setImageForAllStates(_ image: UIImage)**
 	- func titleColorForAllStates(color: UIColor) -> **func setTitleColorForAllStates(_ color: UIColor)**
 	- func titleForAllStates(title: String) -> **func setTitleForAllStates(_ title: String)**


 - **UIColorExtensions**:
 	- init(netHex:Int) -> **init(hex:Int, transparency: CGFloat = 1)**

 - **UIImageExtensions**:
 	- func scaledToHeight(height: CGFloat, with orientation: UIImageOrientation?) -> **scaled(toHeight: CGFloat, with orientation: UIImageOrientation?)**
 	- func scaledToWidth(width: CGFloat, with orientation: UIImageOrientation?) -> **scaled(toWidth: CGFloat, with orientation: UIImageOrientation?)**

 - **UIImageViewExtensions**:
 	- func download(fromUrl: String?, contentMode: UIViewContentMode, placeHolder: UIImage?)) -> **download(from: URL?, contentMode: UIViewContentMode, placeHolder: UIImage?, completionHandler: ((UIImage?, Error?) -> Void)?)**

 - **UISliderExtensions**:
 	- func setValue(value: Float, animated: Bool, duration: TimeInterval, completion: (() -> Void)? = nil) -> **func setValue(_ value: Float, animated: Bool, duration: TimeInterval, completion: (() -> Void)?)**

 - **UITableViewExtensions**:
 	- var totalRows -> **var numberOfRows**

 - **UITextFieldExtensions**:
 	- func setPlaceHolderTextColor(color: UIColor) -> **func setPlaceHolderTextColor(_ color: UIColor)**

 - **UIViewExtensions**:
 	- func loadFromNibNamed(nibNamed: String, bundle : Bundle?) -> **func loadFromNib(named: String, bundle : Bundle?)**

###Removed Extensions:
 - **StringExtensions**:
	 - var locale


## v1.1

UISearchBarExtensions:
 - **textField**: Return the text field inside search bar

UITextFieldExtensions:
 - **setPlaceHolderTextColor(color)**: Change place holder text color
 - **leftViewTintColor**: Left view tint color
 - **rightViewTintColor**: Right view tint color

UINavigationItemExtensions:
 - **replaceTitle(with image)**: Replace title with an image in naivgation item

UITabBarExtensions:
 - **setColors(background, selectedBackground, item, selectedItem)**: Change UITabBar colors

UIImageExtensions:
 - **filled(withColor)**: Return image filled with color
 - **init(color, size)**: Create image from color and size

UITextViewExtensions:
 - **scrollToBotom()**: Scroll to the bottom of text view
 - **scrollToTop()**: Scroll to the top of text view

UISegmentedControlExtensions:
 - **segmentTitles**: Segments titles
 - **segmentImages**: Segments images

UISliderExtensions:
 - **setValue(value, animated, duration, completion)**: Set slide bar value with completion handler

UIAlertControllerExtensions:
 - **show(vibrate)**: Added optional vibration while presenting the alert

IntExtensions:
 - **asLocaleCurrency**: Return string with number and current locale currency

FloatExtensions:
 - **asLocaleCurrency**: Return string with number and current locale currency

DoubleExtensions:
 - **asLocaleCurrency**: Return string with number and current locale currency

StringExtensions:
 - Fixed a bug in toDouble, toFloat, toFloat32, toFloat64 where number is not calculated if not in english

DateExtensions:
 - **adding(component, value)**: Return date by adding a component
 - **nearestHourQuarter**: Return nearest quarter to date
 - **nearestHalfHour**: Return nearest half hour to date
 - **changing(component, value)**: Return date by changing a component
 - Fixed a bug in nearestFiveMinutes, nearestTenMinutes where date was always rounded always to next 5, 10 mins




## v1.0.4

UILabelExtensions:
 - **requiredHeight**: Return required height for a label

UIImageViewExtensions:
 - **blur(withStyle: UIBlurEffectStyle)**: Make image view blurry
 - **blurred(withStyle: UIBlurEffectStyle)**: Return a blurred version of an image view

UINavigationControllerExtensions:
 - **makeTransparent(withTint: UIColor)**: Make navigation controller's navigation bar transparent

UINavigationBarExtensions:
 - **makeTransparent(withTint: UIColor)**: Make navigation controller's navigation bar transparent

UITextFieldExtensions:
 - **trimmedText**: Return text with no spaces or new lines in beginning and end

UIViewExtensions:
 - **addShadow(ofColor, radius, offset, opacity)**: /// Add shadow to view

UIImageExtensions:
- **filled(withColor)**: Return image filled with color

DateExtensions:
- **nearestFiveMinutes**: Return nearest five minutes to date
- **nearestTenMinutes**: Return nearest ten minutes to date

UIViewExtensions:
 - **shake**: Completion handler added to shake function