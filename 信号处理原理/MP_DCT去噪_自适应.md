# 去噪原理
mp算法在DCT字典中选择数个原子组合来还原信号，由于混在信号中的噪声与DCT字典中原子的相干性低，在经过多次迭代后才会被表示。因此设置合适的迭代次数就能不使噪声原子被表示
- 
- 自适应 根据信号自动选择最佳的原子组合原子
-
