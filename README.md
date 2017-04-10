# 常用算法——不同语言的实现
## 直接插入排序
###  python语言的实现 
        def insertSort_f(self,list):
		length=len(list)
		for x in range(1,length):
			if list[x]<list[x-1]:
				temp=list[x]
				print("temp is",temp)
				inx=x-1
				while inx>=0 and list[inx]>temp:
					list[inx+1]=list[inx]
					inx-=1
					print('inx',inx)
				list[inx+1]=temp
				print(list)	
### javascirpt 的实现
		function insertSort(list)
		{
			length=list.length+1;
			for(i=1;i<length;i++){
				if (list[i]<list[i-1]) {
					temp=list[i];
					toMoveIndex=i-1;
					while(list[toMoveIndex]>temp&&toMoveIndex>=0){
						list[toMoveIndex+1]=list[toMoveIndex];
						toMoveIndex--;
					}
					list[toMoveIndex+1]=temp;
				}
			}
			return list;
		}
###  java语言的实现
 		public int [] sort(int [] x){
			int length=x.length+1;
			for(int i=1;i<length;i++){
				if(list[i]<list[i-1]){
					int temp=list[i];
					int toMoveIndex=i-1;
					while(list[toMoveIndex]>temp&&toMoveIndex>=0){
						list[toMoveIndex+1]=list[toMoveIndex];
					}
					list[toMoveIndex+1]=temp;
				}
			}
			return list;
		}
