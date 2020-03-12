# 录音组件的代码片段
特别高兴您愿意抽出时间查看我的简历。由于项目原因暂时无法展示全部的项目代码。
实现效果可以参见：<a target="_blank">https://www.bilibili.com/video/av91827455/</a>
# 这个组件完成了：
- 音频的录制
- 音频的传输
- 音频的动画
# 技术细节
- 音频录制，定义全局录音对象，解决录音时录音对象取不到的问题。方便开发者对录音进行操作。
- 对于音频传输，使用封装了全局的axios请求，分别是<code>server.js</code>(前端请求拦截器)、<code>server.config.js</code>(前端请求配置文件)、<code>api.js</code>(前端请求调用接口文件)。减少了代码量，避免代码冗余，与后期需要修改的麻烦。
- 音频动画，使用CSS3的keyframe、animation动画，并使用transform: translateZ(0)开启了硬件加速。避免使用，width、height、margin等属性，容易引起动画卡顿。
- 独立的录音配置文件，减少代码冗余与修改的麻烦。
- classnames类库的使用，对多个class属性进行管理。
- 使用FormData对象封装Blob文件。
