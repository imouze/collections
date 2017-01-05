#H5页面内层滚动，外层不滚动
--具体解决办法：显示内层时，先把外层的scrollTop保存下来，然后设置position:absolute，然后top设置为scrollTop的负值，等移除内层时再重置为原来的样子
