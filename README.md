＃该数据采集于2018年月初
＃采集自豆瓣
＃在读取csv文件时，关于列表读取有误，请使用以下代码处理
list_col = ['actor','date','director','language','region','type']
for col in list_col:
    df[col] = df[col].apply(lambda x:[i.strip().strip("'") for i in x[1:-1].split(",")])
