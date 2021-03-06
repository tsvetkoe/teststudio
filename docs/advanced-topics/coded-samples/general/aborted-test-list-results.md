---
title: Record Results for Aborted Test List
page_title: Record Results for Aborted Test List
description: "Test Studio is an innovative and easy-to-use automated web, WPF and load testing solution. Test Studio tests support essential technologies like ASP.NET AJAX, Silverlight, PHP and MVC. HTML5, Testing framework, functional testing, performance testing, load testing, exploratory testing, manual testing."
position: 1
---
#Record results even if test list execution is aborted#

*I would like to have results file for the already executed tests if the test list execution is aborted at an earlier stage.*

##Solution##

Test Studio has the ability to store run results on each executed step and this could be turned on within the ***Telerik.TestStudio.Desktop.exe.config*** file. For the default installation, the file could be found in the following folder: *C:\Program Files (x86)\Telerik\Test Studio\Bin*. Open the file in a text editor and set the **'PersistOnEachStep'** key value to True.

> Please note that as of version **2017 R3** the default installation path for new installation is **C:\Program Files (x86)\Progress\Test Studio**.

```XML
  <appSettings>
      <add key="CommandLineRun" value="True" />
      <add key="PersistOnEachStep" value="False" />
  </appSettings>
```

###Command line runner argument###

If you execute tests from <a href="/features/test-runners/artoftest-runner" target="_blank">the command line runner</a> you could set that value to "true" by passing an argument to the command to be executed. The 'PersistOnEachStep' is one of the general options available for modifying the command line test execution behavior. 
