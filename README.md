# How-to-load-xamarin.forms-listview-for-full-height-without-virtualization ?
This example demonstrates how to load xamarin.forms listview for full height without virtualization.

## Sample

```xaml
<ScrollView>
    <StackLayout>
        <syncfusion:SfListView  x:Name="listView1"                                   
                        ItemSpacing="3" 
                        ItemSize="70"     
                            BackgroundColor="AntiqueWhite"
                        ItemsSource="{Binding Contactsinfo}">
            <syncfusion:SfListView.Behaviors>
                <local:ListViewBehavior/>
            </syncfusion:SfListView.Behaviors>
            <syncfusion:SfListView.ItemTemplate>
                <DataTemplate>
                    <ViewCell>
                        <ViewCell.View>
                            <Grid x:Name="grid" RowSpacing="1">
                                <Grid.RowDefinitions>
                                    <RowDefinition Height="*" />
                                    <RowDefinition Height="1" />
                                </Grid.RowDefinitions>
                                <Grid RowSpacing="1">
                                    <Grid.ColumnDefinitions>
                                        <ColumnDefinition Width="*" />
                                        <ColumnDefinition Width="70" />
                                    </Grid.ColumnDefinitions>

                                    <Grid Grid.Column="0"
                                        RowSpacing="1"
                                        Padding="10,0,0,0"
                                        VerticalOptions="Center">
                                        <Grid.RowDefinitions>
                                            <RowDefinition Height="*" />
                                            <RowDefinition Height="*" />
                                        </Grid.RowDefinitions>

                                        <Label LineBreakMode="WordWrap"
                                            
                                            Text="{Binding ContactName}">
                                        </Label>
                                        <Label Grid.Row="1"
                                            Grid.Column="0"
                                            
                                            
                                            Text="{Binding ContactNumber}">
                                        </Label>
                                    </Grid>
                                </Grid>
                                <StackLayout Grid.Row="1" BackgroundColor="Gray" HeightRequest="1"/>
                            </Grid>
                        </ViewCell.View>
                    </ViewCell>
                </DataTemplate>
            </syncfusion:SfListView.ItemTemplate>
        </syncfusion:SfListView>
        <BoxView HeightRequest="5" BackgroundColor="Red"/>
        <syncfusion:SfListView  x:Name="listView2"                                   
                        ItemSpacing="3" 
                        ItemSize="70"                                             
                                BackgroundColor="FloralWhite"
                        ItemsSource="{Binding Contactsinfo}">
            <syncfusion:SfListView.Behaviors>
                <local:ListViewBehavior/>
            </syncfusion:SfListView.Behaviors>
            <syncfusion:SfListView.ItemTemplate>
                <DataTemplate>
                    <ViewCell>
                        <ViewCell.View>
                            <Grid x:Name="grid" RowSpacing="1">
                                <Grid.RowDefinitions>
                                    <RowDefinition Height="*" />
                                    <RowDefinition Height="1" />
                                </Grid.RowDefinitions>
                                <Grid RowSpacing="1">
                                    <Grid.ColumnDefinitions>
                                        <ColumnDefinition Width="*" />
                                        <ColumnDefinition Width="70" />
                                    </Grid.ColumnDefinitions>

                                    <Grid Grid.Column="0"
                                        RowSpacing="1"
                                        Padding="10,0,0,0"
                                        VerticalOptions="Center">
                                        <Grid.RowDefinitions>
                                            <RowDefinition Height="*" />
                                            <RowDefinition Height="*" />
                                        </Grid.RowDefinitions>

                                        <Label LineBreakMode="WordWrap"
                                            
                                            Text="{Binding ContactName}">
                                        </Label>
                                        <Label Grid.Row="1"
                                            Grid.Column="0"
                                            
                                            
                                            Text="{Binding ContactNumber}">
                                        </Label>
                                    </Grid>
                                </Grid>
                                <StackLayout Grid.Row="1" BackgroundColor="Gray" HeightRequest="1"/>
                            </Grid>
                        </ViewCell.View>
                    </ViewCell>
                </DataTemplate>
            </syncfusion:SfListView.ItemTemplate>
        </syncfusion:SfListView>
    </StackLayout>
</ScrollView>
```

## <a name="requirements-to-run-the-demo"></a>Requirements to run the demo ##

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) or [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/).
* Xamarin add-ons for Visual Studio (available via the Visual Studio installer).

## <a name="troubleshooting"></a>Troubleshooting ##
### Path too long exception
If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.
