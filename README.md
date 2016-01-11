# ChromeDriver
Rebuild chromedriver.exe with support for XWalk WebViews.

How to use with appium:

1) Replace ..\Appium\node_modules\appium\node_modules\appium-chromedriver\chromedriver\win\chromedriver.exe with the chromedriver.exe 
provided here.

2) Edit the androidHybrid.listWebviews method in ..\Appium\node_modules\appium\lib\devices\android\android-hybrid.js to 
push {package name}_devtools_remote to the webviews list. The modified android-hybrid.js is provided in the reposistory.

3) Ensure that you have remote debugging enabled in your WebView.

4) Set the driver context to the webview. 

  Set<String> contextNames = driver.getContextHandles();
  driver.context((String) contextNames.toArray()[1]); // set context to WEBVIEW_{appPackage}
