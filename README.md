/*You have a 2d array.Please write a program for finding column's number
with maximal average of elements. */

#include <stdio.h>
int main(){

	int i,j, col, sum;
	int arr[2][4] = {
		{10, 11, 12, 13},
		{14, 15, 16, 17}
	};

	float average, max;

	for(j =0;j<4;j++){
		sum=0;
		for(i =0; i<2; i++){
			sum += arr[i][j];
		}

		average = sum/2;

		if(average> max){
			max=average;
			col = j+1;
		}
		}
	printf("Column's number with maximal average of elements: %d", col);
	return 0;
}
