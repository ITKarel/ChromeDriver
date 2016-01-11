# ChromeDriver
Rebuild chromedriver.exe with support for XWalk WebViews.

How to use with appium:

1) Replace ..\Appium\node_modules\appium\node_modules\appium-chromedriver\chromedriver\win\chromedriver.exe with the chromedriver.exe 
provided here.

2) Edit the androidHybrid.listWebviews method in ..\Appium\node_modules\appium\lib\devices\android\android-hybrid.js to 
push {package name}_devtools_remote to the webviews list. 

