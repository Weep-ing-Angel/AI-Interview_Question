1. 手撕二维矩阵相乘
def matrix_multiply(A, B):
    # 获取矩阵 A 和 B 的尺寸
    n = len(A)
    m = len(B[0])
    k = len(B)
    
    # 创建结果矩阵 C，尺寸为 (n, m)
    C = [[0] * m for _ in range(n)]
    
    # 执行矩阵乘法
    for i in range(n):
        for j in range(m):
            C[i][j] = sum(A[i][p] * B[p][j] for p in range(k))
    
    return C
