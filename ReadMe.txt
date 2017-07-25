2017-07-14：完成相机校准

2017-07-16：Vertical+Horizontal扫描方式有问题，TrianguatorWorker经常出现帧冲突，可能是图片抓取太快，TriangulatorWorker结算时间太长导致的
	    triangulateFromUpVp()尚未完全完成，所有V+H方式扫描重建效果很差
	    只用V和只用H方式重建效果相当，但都有毛刺，
	    当前测试都是在2X3相移编码器下，即相移图案为3帧空间周期16的黑白条纹和3帧空间周期为1的黑白条纹

2017-07-18：测试3PhaseShift、4PhaseShift、NPhaseShift正常工作
			3PhaseShiftUnwrap一直无点云图像输出，不知道是否解相的问题
			修正3PhaseShiftFastWrap的段错误

2017-07-20：修正3PhaseShiftUnwrap问题
	    多次出现显示异常，重建模型也都不对了，depth图也不清楚
	    多处抛出异常。。。
		
2017-07-25：修正线程异常：SLVideoDialog 注释QCoreApplication::processEvents()
			修正3PhaseShiftUnwrap的Mat使用错误
			经测试，只有4相移编码器下会出现点云模型一闪而过的情况，3\3F\3U\N\2X3在QVTK中正常显示
