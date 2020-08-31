# python-visualization
## np應用於繪圖
0.1 meshgrid(list,list)  
0.2 histgram(list,bins)輸出counts,bin_edge  
0.3 histogram2d(list,list,bins)輸出counts,xedge,yedge  
## matplotlib.pyplot
### 外框顯示
1.1 style.use  
1.2 show  
1.3 figure(figsize)  
1.3.1 add_axes(list,xticklabels,ylim)  
1.3.2 add_subplot(nrow,ncol,number)or add_subplot(1.7,xticklabels,sharey)  
1.3.3 subplots_adjust(hspace,wspace)  
1.3.4 fig.transFigure  
1.3.5 savefig  
1.4 axes(list,xscale,yscale,axisbg,projection='3d')  
1.4.1 plot  
1.4.2 set(xlim,ylim,xlabel,ylabel,title,xticks,yticks)  
1.4.3 axis  
1.4.4 legend(loc,frameon,ncol,fancybox,framealpha,shadow,borderpad)  
1.4.5 add_artist(legend)  
1.4.6 imshow  
1.4.7 ax.transData,ax.transAxes,  
1.4.8 set_xlim(number,number),set_ylim(number,number)  
1.4.9 xaxis.set_major_locator(4.3 or 6.2)  
1.4.10 xaxis.set_minor_locator(4.3 or 6.2)  
1.4.11 xaxis.set_major_formatter(4.3 or 6.2)  
1.4.12 xaxis.set_minor_formatter(4.3 or 6.2)  
1.4.13 grid(True or False)  
1.4.14 set_axisbelow(True or False)  
1.4.15 get_xticklabels
1.4.15.1 set(weight,color)  
1.4.16 axvline(number,alpha,color)  
1.4.17 set_alpha  
1.5 subplots(nrow,ncol,sharex,sharey,figsize,facecolor,subplot_kw=dict,gridspec_kw=dict)輸出figure&axes   
1.5.1 flat(axes屬性)  
1.6 subplot(nrow,ncol,number)輸出figure&axes or subplot(1.7)  
1.7 GridSpec(nrow,ncol,hspace,wspace)  
1.8 invert_yaxis  
1.9 invert_xaxis  
1.10 grid  
1.11 rc  
### 軸與標題
2.1 clabel(圖片,inline,fontsize)  
2.2 xlim(number,number)  
2.3 ylim(number,number)  
2.4 axis(list or "tight" or "equal")  
2.5 title  
2.6 xlabel  
2.7 ylabel  
2.8 clim  
2.9 xticks(rotation)  
### 圖例顯示
3.1 colorbar(ticks,label)  
3.1.1 set_label  
3.2 legend  
### 內部文字箭頭
4.1 text(number,number,text,fontsize,ha,transform=1.3.4 or 1.4.7)  
4.2 annotate(str,xy=tuple,xytext=tuple,arrowprops=dict(facecolor,shrink,arrowstyle,connectionstyle))  
4.3 NullFormatter(),NullLocator(),MaxNLocator(3),MultipleLocator(),FuncFormatter(function)  
### eda圖形種類
5.1 contour(list,list,list,colors,cmap)  
5.2 contourf(list,list,list,colors,cmap)  
5.3 imshow(extend=list,origin,cmap,alpha)  
5.4 hist(list,bins=number or list,normed,alpha,histtype,color,edgecolor)  
5.5 plot(list,list,linestyle,color,label,markersize,linewidth,markerfacecolor,markeredgecolor,markeredgewidth)  
5.6 hist2d(list,list,bins,cmap)  
5.7 hexbin(list,list,gridsize,cmap)  
5.8 scatter(list,list,marker,c,s,alpha,cmap)  
5.9 pie(list,explode,labels,colors,labeldistance,autopct,shadow,radius,startangle,pctdistance)  
5.10 errorbar(list,list,yerr=number,fmt)  
5.11 fill_between(list,list,list,color,alpha)  
####  mpl_toolkits mplot3d
5.12 plot3D(list,list,list)  
5.13 scatter3D(list,list,list,c,cmap)  
5.14 contour3D(list,list,list,cmap)  
5.15 plot_wireframe(list,list,list,color)  
5.16 plot_surface(list,list,list,rstride,cstride,cmap,edgecolor)  
5.17 plot_trisurf(list,list,list,cmap,edgecolor)  
## matplotlib
6.1 rcParams\['font.size'\]  
6.2 dates.MonthLocator(),dates.MonthLocator(bymonthday=15),dates.DateFormatter('%h')  
# matplotlib.legend
## Legend
Legend(ax,list(lines),list(labels),loc,frameon)  
# matplotlib  
## cycler  
cycler("color",list)  
## seaborn  
### 基本設定
7.1 set  
7.2 axes_style  
### eda圖形種類
8.1 kdeplot(list,shade,label)  
8.2 distplot(list,label)  
8.3 jointplot(columns,columns,data,kind="kde" or "hex")  
8.4 pairplot(data,hue,size)  
8.5 FacetGrid(data,row,col,margin_titles)  
8.5.1 map(plt繪圖,column)  
8.6 factorplot(x,y,z,data,kind="box") or factorplot(x,data,aspect,kind="count",color,hue,order)  
8.6.1 set_axis_labels  
8.6.2 set_xticklabels(step=number)  
8.6.3 set_ylabels  
8.7 barplot(X,y)  
8.8 heatmap(data,cmap,vmin,annot,vmax)  
8.9 PairGrid(data,size,diag_sharey,hue,vars=list)  
8.9.1 map_upper,map_diag,map_lower  
8.10 lmplot(x,y,hue,data,fit_reg)  
8.11 regplot(x,y)  
8.12 boxplot(x,y,data,palette=list,hue)  
# wordcloud
## WordCloud
9.1 WordCloud(background_color)  
9.1.1 generate(text)  
## plotly
plotly.offline.init_notebook_mode(connected=True)  
plotly.offline.iplot(dict("data":data,"layout":Layout(title)))  
# from plotly.graph_objs
## Scatter:線型圖和散點圖 Bar:長條圖 Histogram:直方圖 Pie:圓餅圖 Box:箱型圖 Scattergeo:一般地圖
Scatter(x,y,text,textposition,mode,name)  
*其他套件from IPython.display import Image,from matplotlib.image import imread
