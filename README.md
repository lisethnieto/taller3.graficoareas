# taller3.graficoareas
import pandas as pd 
import matplotlib.pyplot as plt
import numpy as np

fig,axes = plt.subplots(2,1,figsize = (8,6))
plt.title("ejemplo1 areas  ")
df1 = pd.DataFrame(np.random.rand(10, 4), columns=['a', 'b', 'c', 'd'])
df2 = pd.DataFrame(np.random.randn(10, 4), columns=['a', 'b', 'c', 'd'])

df1.plot.area(colormap = 'Greens_r',alpha = 0.5,ax = axes[0])
df2.plot.area(stacked=False,colormap = 'Set2',alpha = 0.5,ax = axes[1])


fig,axes = plt.subplots(5,2,figsize = (8,6)) 

x = np.linspace(0, 1, 500)
y1 = np.sin(4 * np.pi * x) * np.exp(-8 * x)
y2 = -np.sin(4 * np.pi * x) * np.exp(-8 * x)
y3 = np.tan(4 * np.pi * x) * np.exp(-5 * x)
y4 = -np.tan(4 * np.pi * x) * np.exp(-5* x)
y5 = np.cos(4 * np.pi * x) * np.exp(-5 * x)
y6 = -np.cos(4 * np.pi * x) * np.exp(-5* x)
y7 = np.sin(4 * np.pi * x) * np.exp(-5 * x)
y8 = -np.cos(4 * np.pi * x) * np.exp(-5* x)
y9 = np.tan(4 * np.pi * x) * np.exp(-5 * x)
y10 = -np.sin(4 * np.pi * x) * np.exp(-5* x)


axes[0,0].fill(x, y1, 'r',alpha=0.5,label='y1') 
axes[0,0].fill(x, y2, 'g',alpha=0.5,label='y2')
axes[1,0].fill(x, y3, 'r',alpha=0.5,label='y3')
axes[1,0].fill(x, y4, 'g',alpha=0.5,label='y4')
axes[2,0].fill(x, y5, 'r',alpha=0.5,label='y5')
axes[2,0].fill(x, y6, 'g',alpha=0.5,label='y6')
axes[3,0].fill(x, y7, 'r',alpha=0.5,label='y7')
axes[3,0].fill(x, y8, 'g',alpha=0.5,label='y8')
axes[4,0].fill(x, y9, 'r',alpha=0.5,label='y9')
axes[4,0].fill(x, y10, 'g',alpha=0.5,label='y10')



x = np.linspace(0, 5 * np.pi, 1000) 
y1 = np.sin(x)  
y2 = np.sin(2 * x)  
y3 = np.tan(x)  
y4 = np.tan(2 * x)  
y5 = np.cos(x)  
y6 = np.cos(2 * x) 
y7 = np.sin(x)  
y8 = np.cos(2 * x)   
y9 = np.tan(x)  
y10= np.sin(2 * x)  

axes[0,1].fill_between(x, y1, y2, color ='blue',alpha=0.5,label='area') 
axes[1,1].fill_between(x, y3, y4, color ='orange',alpha=0.5,label='area')  
axes[2,1].fill_between(x, y5, y6, color ='purple',alpha=0.5,label='area')  
axes[3,1].fill_between(x, y7, y8, color ='yellow',alpha=0.5,label='area')  
axes[4,1].fill_between(x, y9, y10, color ='red',alpha=0.5,label='area')  

plt.show()

