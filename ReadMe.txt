2017-07-14：完成相机校准

2017-07-16：Vertical+Horizontal扫描方式有问题，TrianguatorWorker经常出现帧冲突，可能是图片抓取太快，TriangulatorWorker结算时间太长导致的
	    triangulateFromUpVp()尚未完全完成，所有V+H方式扫描重建效果很差
	    只用V和只用H方式重建效果相当，但都有毛刺，
	    当前测试都是在2X3相移编码器下，即相移图案为3帧空间周期16的黑白条纹和3帧空间周期为1的黑白条纹

2017-07-18：测试3PhaseShift、4PhaseShift、NPhaseShift正常工作
			3PhaseShiftUnwrap一直无点云图像输出，不知道是否解相的问题
			修正3PhaseShiftFastWrap的段错误
