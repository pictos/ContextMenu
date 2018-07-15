# ContextViewCell control for Xamarin Forms

## Setup
* Available on NuGet: [ContextViewCell](http://www.nuget.org/packages/ContextViewCell) [![NuGet](https://img.shields.io/nuget/v/ContextViewCell.svg?label=NuGet)](https://www.nuget.org/packages/ContextViewCell)
* Add nuget package to your Xamarin.Forms .netStandard/PCL project and to your platform-specific projects (iOS and Android)

|Platform|Version|
| ------------------- | ------------------- |
|Xamarin.iOS|8.0+|
|Xamarin.Android|15+|

## ContextViewCell
This plugin provides opportunity to create custom context menu for every cell

![Sample GIF](https://media.giphy.com/media/pP3bDaKCnu8z1okVNn/giphy.gif)


## Samples
The sample you can find here https://github.com/AndreiMisiukevich/ContextMenu/blob/master/ContextMenuSample/ContextMenuSample/SamplePage.xaml

**XAML:**
```xml
    <ListView>
        <ListView.ItemTemplate>
            <DataTemplate>
                <context:ContextViewCell>
                    <context:ContextViewCell.Content>
                        //{YOUR MAIN VIEW HERE}
                        </ContentView>
                    </context:ContextViewCell.Content>
                    <context:ContextViewCell.ContextTemplate>
                        <DataTemplate>
                            //{YOUR CONTEXT TEMPLATE HERE} you can use DataTemplateSelector too
                        </DataTemplate>
                    </context:ContextViewCell.ContextTemplate>
                </context:ContextViewCell>
            </DataTemplate>
        </ListView.ItemTemplate>
    </ListView>
```
*Make sure your main view width equals list's width*
You can adjust it by binding

```xml
...
<ListView x:Name="SampleList"
        <ListView.ItemTemplate>
            <DataTemplate>
                <context:ContextViewCell>
                    <context:ContextViewCell.Content>
                        <ContentView WidthRequest="{Binding Source={x:Reference SampleList}, Path=Width}">
                            ...
```

**C#:**

The sample you can find here https://github.com/AndreiMisiukevich/ContextMenu/blob/master/ContextMenuSample/ContextMenuSample/CodeSamplePage.cs

Check source code for more info, or 🇧🇾 ***just ask me =)*** 🇧🇾

## License
The MIT License (MIT) see [License file](LICENSE)

## Contribution
Feel free to create issues and PRs 😃

