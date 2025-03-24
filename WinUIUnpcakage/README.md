### AOT

`dotnet publish -p:PublishAot=true -o bin/publish` to generate native executable.

### SingleFile

`dotnet publish -p:WindowsPackageType=None -p:PublishSingleFile=true -o bin/single`

could not properly launch

```
Application: WinUIUnpcakage.exe
CoreCLR Version: 9.0.225.6610
.NET Version: 9.0.2
Description: The process was terminated due to an unhandled exception.
Exception Info: System.Runtime.InteropServices.COMException (0x80040111): ClassFactory 无法供应请求的类

   at System.Runtime.InteropServices.Marshal.ThrowExceptionForHR(Int32 errorCode)
   at WinRT.ActivationFactory.Get(String typeName, Guid iid)
   at Microsoft.UI.Xaml.Application.get__objRef_global__Microsoft_UI_Xaml_IApplicationStatics()
   at Microsoft.UI.Xaml.Application.Start(ApplicationInitializationCallback callback)
   at WinUIUnpcakage.Program.Main(String[] args)
```