Q: 香山core coremark 跑分是多少呢？

A: Currently (20210701) 5.3 CoreMark/MHz，gcc 9.3，-O2

Q: 从中国大陆下载速度过慢怎么办？

A: 请使用中国大陆的镜像：

CSDN - https://codechina.csdn.net/OpenXiangShan

Gitee - https://gitee.com/OpenXiangShan

Q: 如何调整香山的配置？

A: 修改香山的配置可以参考这个文件中 MinimalConfig 的处理方式, 在构建自己的 Config 的时候只需要将与默认配置不同的部分写在 Config 里即可:

https://github.com/OpenXiangShan/XiangShan/blob/master/src/main/scala/top/Configs.scala

使用类似的方式定义自己的 Config 之后可以在生成 Verilog /仿真时使用 CONFIG 参数确定使用哪种配置. 例如: `make emu CONFIG=MinimalConfig`.

香山的默认参数放在这个文件里, 一般不建议修改:

https://github.com/OpenXiangShan/XiangShan/blob/master/src/main/scala/xiangshan/Parameters.scala

香山的参数系统使用了 Context-Dependent Evironments 这个参数环境, 对应仓库中的 api-config-chipsalliance 这个 submodule. 更详细的使用说明可以参考这个仓库的文档:

https://github.com/chipsalliance/api-config-chipsalliance

Q: 生成香山核建议使用多大内存？
A: 64G