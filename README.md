这个仓库就是放spine动画资源测试小程序情况的，因为ihub里不允许放3.8版本的skel文件，特此建个项目来存，直接通过路径访问，白嫖个服务器
gotoPlay(e){
    // 保存全局参数位置：globalData.pageParams['3.8'].assets
    let version = 3.8
    let assets = {
        "raptor": {
            "atlas": "https://zheng834386282.github.io/resources/spine38assets/raptor-pma.atlas",
            "texture": "https://zheng834386282.github.io/resources/spine38assets/raptor-pma.png",
            "type": "skel",
            "skel": "https://zheng834386282.github.io/resources/spine38assets/raptor-pro.skel"
        }
    }
    globalData.pageParams = { [version]: { "assets": assets} };
    wx.navigateTo({ url: `/pages/spine-player/spine-player?version=${version}` });
},
