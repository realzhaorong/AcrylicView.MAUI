
|支持平台/Supported platforms        |
|----------------------------|
| :heavy_check_mark: Android | 
| :heavy_check_mark: iOS     |
| :heavy_check_mark: macOS   |
| :heavy_check_mark: Windows |


NugetPackage：AcrylicView.Maui

![231667033-e99ed65b-d74a-4e70-9e89-0958afdc5e45](https://github.com/sswi/AcrylicView.MAUI/assets/39110708/1e05f06c-7d43-403a-8f83-74d9436c44f3)
MauiProgram.cs

```csharp

using Xe.AcrylicView;

    public static class MauiProgram
    {
        public static MauiApp CreateMauiApp()
        {
            var builder = MauiApp.CreateBuilder();
            builder
                .UseMauiApp<App>()
                
                .UseAcrylicView()  //*********  usage
                
                
                .ConfigureFonts(fonts =>
                {
                    fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
                    fonts.AddFont("OpenSans-Semibold.ttf", "OpenSansSemibold");
                });
            return builder.Build();
        }
    }
}
```



 
```xml
 xmlns:ui="clr-namespace:Xe.AcrylicView;assembly=Xe.AcrylicView" 

<ui:AcrylicView VerticalOptions="Center"  
                HeightRequest="100"  
                EffectStyle="Custom"    
                Margin="10"  
                TintColor="OrangeRed" 
                TintOpacity=".15 "  
                BorderColor="OrangeRed" 
                BorderThickness="1,2" 
                CornerRadius="50,10,30,20"
                >           
   <Grid>
    <Label Text="Hello Word" FontSize="25" HorizontalOptions="Center" VerticalOptions="Center" TextColor="OrangeRed"/>    
   </Grid>
</ui:AcrylicView>
```



Android平台的实现方式是从这个仓库获取，从Xamarin.Forms简单移植过来的，请支持原作者：
https://github.com/roubachof/Sharpnado.MaterialFrame
