## 配置 vscode + picgo + GitHub 实现自动上传图片
blogimages

### GitHub设置
新建仓库用作存放图库，设置连接 token

`Setting`/`Developer Settings`/`Personal access tokens`

点击`Generate new token (classic)`，注意选择 ***classic*** 类型

![20240112172808_2024-01-12-17-28-09](https://raw.githubusercontent.com/kaerser/blogimages/main/img/20240112172808_2024-01-12-17-28-09.png)

按以下权限进行设置，关注过期时间，一般选择 ***90天***，生成之后就不可查看，注意复制保存
![20240112173158_2024-01-12-17-31-59](https://raw.githubusercontent.com/kaerser/blogimages/main/img/20240112173158_2024-01-12-17-31-59.png)

### vscode 设置
插件中搜索并安装`Picgo`，设置插件

`Custom upload Name` -> `${fileName}_${dateTime}${extName}`

![20240112173652_2024-01-12-17-36-53](https://raw.githubusercontent.com/kaerser/blogimages/main/img/20240112173652_2024-01-12-17-36-53.png)

`Current` -> `github`

`Branch` -> `main`

`Path` -> `img/` （自定义设置的存储路径）

`Repo` -> `kaerser/blogimages`

`Token` -> `前文生成的token串`

![20240112173844_2024-01-12-17-38-45](https://raw.githubusercontent.com/kaerser/blogimages/main/img/20240112173844_2024-01-12-17-38-45.png)

>如果本地不能访问GitHub，需要通过代理的话，设置 vsconde http 代理进行访问
> 
> `Setting` / `Application` / `Proxy` 

![20240112174612_2024-01-12-17-46-14](https://raw.githubusercontent.com/kaerser/blogimages/main/img/20240112174612_2024-01-12-17-46-14.png)


### 自动上传图片

vscode 中新建 md 文件。

- 截图上传，快捷键 `Ctrl + Alt + U` 
- 本地文件夹上传，快捷键 `Ctrl + Alt + E`

上传完成之后 md 文件中会自动生成图片的连接，可以直接使用
![20240112175030_2024-01-12-17-50-31](https://raw.githubusercontent.com/kaerser/blogimages/main/img/20240112175030_2024-01-12-17-50-31.png)

GitHub 中也会存在相应的文件

