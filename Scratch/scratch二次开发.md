# 基于scratch的二次开发
- 项目结构

![](img/scratch项目结构.png)  

![](img/项目结构.png)

## 自定义品牌logo
![](img/品牌logo.png)  

menu-bar里存储了logo的静态资源，同时在menu-bar.jsx中引入该资源进而设置好自己的logo  

![](img/mylogo.png)  

![](img/logo引入.png)  

```
import minicodeLogo from './minicode-logo.png';

<div className={classNames(styles.menuBarItem)}>
    <img
        alt="Minicode"
        className={classNames(styles.minicodeLogo, {
            [styles.clickable]:
                typeof this.props.onClickLogo !== 'undefined'
        })}
        draggable={false}
        src={minicodeLogo}
        onClick={this.props.onClickLogo}
    />
</div>
```

![](img/menu-bar.png)  

menu-bar.jsx中设置了该导航栏的相关设置

## 自定义用户系统
- reducers/gui.js中设置项目用户相关的初始化信息
- components/gui/gui.jsx定义的GUIComponent组件定义了整个项目的基本样式结构
- reducers/mini-login.js用户登录信息
- mini-global/login-context.js登录相关逻辑