# 事件转命令
>WPF中将事件包装成命令在ViewModel中进行处理

xaml代码
``` cs
xmlns:i="http://schemas.microsoft.com/expression/2010/interactivity"

        <TextBox Margin="203,117,199,145" Name="textBox">
            <i:Interaction.Triggers>
                <i:EventTrigger EventName="KeyDown">
                    <i:InvokeCommandAction
                        Command="{Binding Path=DataContext.UnCheckedCommand, ElementName=self}"
                        CommandParameter="{Binding ElementName=textBox}" />
                </i:EventTrigger>
            </i:Interaction.Triggers>
        </TextBox>
```
# 添加右键菜单
每个xaml节点都有个ContextMenu属性

``` cs
<ListViewItem.ContextMenu>
    <ContextMenu>
        <MenuItem Header="使用" />
        <MenuItem Header="添加" />
        <MenuItem Header="移除" />
    </ContextMenu>
</ListViewItem.ContextMenu>
```
