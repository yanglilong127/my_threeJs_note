WebGL能做什么？ 

游戏
家具
虚拟地图
城市地图
CAD制图


几何体THREE.Geometry();
几何体是一个包含必要三维数据的一个数据结构:
点：this.vertices = [];
颜色：this.colors = [];
面： this.faces = [];

var geometry = new THREE.Geometry();
geometry.vertices.push(
	new THREE.Vector3(-10,10,0),
	new THREE.Vector3(-10,-10,0),
	new THREE.Vector3(10,-10,0)
);


线材质THREE.LineBasicMaterial
简单的说就是物体看起来是什么质地。材质可以看成是材料和质感的结合。在程序中，它是表面各可视属性的结合，这些可视属性是指表面的色彩、纹理、光滑感、透明度、反射率、折射率、发光度等。

LineBasicMaterial(参数对象);
color：线条的颜色，用16进制来表示，默认的颜色是白色。

linewidth：线条的宽度，默认时候1个单位宽度。

linecap：线条两端的外观，默认是圆角端点，当线条较粗的时候才看得出效果，如果线条很细，那么你几乎看不出效果了。

linejoin：两个线条的连接点处的外观，默认是“round”，表示圆角。

vertexColors：定义线条材质是否使用顶点颜色，这是一个boolean值。意思是，线条各部分的颜色会根据顶点的颜色来进行插值。（如果关于插值不是很明白，可以QQ问我，QQ在前言中你一定能够找到，嘿嘿，虽然没有明确写出）。

fog：定义材质的颜色是否受全局雾效的影响。


性能测试：
fps：视频或者动画每秒显示多少帧数，
理论上，3D程序最大的帧数是显卡支持的刷新率，一般是60；
游戏最好在30fps以上

Stat一个监控程序帧数、每秒时间、内存使用量的js库
https://github.com/mrdoob/stats.js
监控内存： --enable-precise-memory-info


工具渐变类 Tween.js
new TWEEN.Tween(camera.position)
	.to({x:400},3000).repeat(Infinity).start();
在3000毫秒内使相机的x左边变为400,并一直重复