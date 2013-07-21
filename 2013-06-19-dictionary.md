Title: python 字典 
Category:  编程学习 
Tags: python

##字典 key - value
	>>> d ={} # 一个空的字典
	>>> d['a'] = 'alpha'
	>>> d['o'] = 'omega'
	>>> d['g'] = 'gamma'
	
根据key，返回字典中的value
	
	>>> d.get('a')
	'alpha'

判断key是否在字典中
	
	>>> 'a' in d
	True

得到字典中的key

	>>> d.keys()
	dict_keys(['o', 'a', 'g'])
	
得到字典中的values
	
	>>> d.values()
	dict_values(['omega', 'alpha', 'gamma'])
	

打印出字典中所有的key-value

	>>> for k in sorted(d.keys()):
	print('key:',k,'->',d[k])

	
	key: a -> alpha
	key: g -> gamma
	key: o -> omega


