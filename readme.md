# 新手学习 webpack 的练习 Demo
> 整个项目主要学习自 [coderwhy老师这个课程](https://ke.qq.com/course/3453141#term_id=104002353)

## 食用方式
项目根目录下有`note.md`文件，这个是我的笔记文件，大家可以参考这个文件，一步一步练起来，对webpack有个初步的了解。

**建议（重要）**

线上仓库没有删除`package.json`和`package-lock.json`这两个文件，仓库git到本地后，建议直接将这两个文件改名为`package_backup.json`和`package-lock_backup.json`，然后自己`npm init -y`新建这两个文件，让后参考笔记一步一步安装对应依赖（**这个过程对于学习webpack非常重要，也非常有用**）。

另外`webpack.config.js`这个文件配置部分我注释了，大家学习的时候，直接打开对应部分注释即可，如果可以的话，也建议先备份这个文件，自己手动创建再敲一遍，这样印象深刻。

## 个人理解
学webpack主要是理解配置文件中的几个属性：
- `配置入口`：打包的入口文件，通过这个文件建立项目资源依赖图。
- `配置出口`：打包出口，就是打包好了放到哪里，没啥好说的。
- `Loaders`：对于不同资源（个人狭义理解就是对于不同后缀名文件`例如： .css .less .ts .vue ...`）进行处理，可以理解为让webpack认识这种类型文件，处理这种类型文件。
- `Plugins`：如果你想在webpack打包过程中进行一些操作，就可以使用插件（例如本demo中在执行打包命令后，每次打包前自动先删除之前打包好的目录文件的功能，就可以用`clean-webpack-plugin`这个插件）。这个可以类比`Vue`中组件的`生命周期钩子`思想，在组件的不同阶段，会自动帮你调用生命周期钩子，类比到webpack中就是在特定时刻会使用你配置的插件。