// 패턴기억.cpp : 콘솔 응용 프로그램에 대한 진입점을 정의합니다.
//

#include "stdafx.h"
#define row 3
#define col 3

int main()
{
	int matrix_save[row * col] = { 1, 1, 1, -1, -1, 1, -1, -1, 1 };
	//int matrix_save[row * col] = {1, -1, -1, -1, 1, -1, -1, -1, 1, -1, -1, -1, 1, 1, 1, 1 }; // row 4 col 4 ㄴ자 테스트용 패턴
	int matrix_input[row * col];
	int matrix0[row * col][row * col];// matrix_save * matrix_save^t
	int matrix_out[row * col];
	int tmp;

	for (int i = 0; i < row * col; i++) {//matrix0 정의
		for (int j = 0; j < row * col; j++) {
			matrix0[i][j] = matrix_save[i] * matrix_save[j];
		}
	}

	printf("패턴 입력 (%d * %d)▽\n", row, col);
	for (int i = 0; i < row * col; i++) {
		scanf_s("%d", &matrix_input[i]);
	}

	printf("\n=============결과==================\n");

	for (int i = 0; i < row * col; i++) {//matrix_out 정의 및 출력
		tmp = 0;
		for (int j = 0; j < row * col; j++) {
			tmp += matrix_input[j] * matrix0[i][j];
		}

		if (tmp > 0) {
			matrix_out[i] = 1;
		}
		else if (tmp < 0) {
			matrix_out[i] = -1;
		}

		if (matrix_out[i] == 1) {
			printf("■");
		}
		else if (matrix_out[i] == -1) {
			printf("□");
		}
		else {
			printf("★");//error
		}

		if ((i + 1) % row == 0 && i != 0) {
			printf("\n");
		}
	}
    return 0;
}
}
