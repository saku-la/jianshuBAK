> CSV格式文件是以逗号为分割符的文本文件，程序读取的是示波器保存的数据，通过文本文件操作实现

```
# 读取示波器保存的数据，得到幅值
# 将csv格式文件保存到data列表中
import matplotlib.pyplot as plt
import pickle

def convert_csv(csv):
    data=[]
    data_str=''
    with open(csv) as f_csv:
        for i, row in enumerate(f_csv):
            s=row.split(',')
            try:
                data_str+=s[-2]
                data.append(float(s[-2]))
            except:
                print(i)
                break
    return data

# data = convert_csv('F0000CH1.CSV')
# 保存文件
# with open('data01.txt', 'w') as f:
    # f.write(data_str)

# with open ('data01.plk','wb') as f:
    # pickle.dump(data, f)

# 绘图
plt.plot(data)
plt.show()
```
