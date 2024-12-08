# C#/WinRT Projection Sample with a Xaml Control

This package is an updated projection sample for targeting Windows Desktop Apps using the Windows App SDK and WinUI3, which is simply
a merge of the two walkthoughs below.  As part of the update, I've recreated the projects using the latest project
templates, and then ported the code from the Microsoft Samples. 

The first project is a Windows Runtime Component for Desktop Apps, based on the WinUI 3 Controls Library. It includes the SimpleMath
class from the original sample, and the BgLabelControl from the C++ templated control sample.

The second project is a CSWinRT Projection library.

Main takeaways:

- Be sure to update the native Platform RID's (win10-z64 -> win-x64) .nuspec
- Include the .pri file alongside the control .dll in the NuGet runtimes\win-x64\native\ folder
- Include a reference to the WindowsAppSDK in the projection project
- Make sure to use the proper namespaces for WinUI ( Microsoft.UI.Xaml not Windows.UI.Xaml)


See also:

- Generate a C# projection from a C++/WinRT component, distribute as a NuGet for .NET apps [https://learn.microsoft.com/en-us/windows/apps/develop/platform/csharp-winrt/net-projection-from-cppwinrt-component]
- XAML custom (templated) controls with C++/WinRT [https://learn.microsoft.com/en-us/windows/uwp/cpp-and-winrt-apis/xaml-cust-ctrl]
