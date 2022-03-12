#include<iostream>
#include <stdio.h>
#include <string.h>
#include<stdlib.h>
#include <string>
using namespace std;
void add(float A[][10], float B[][10], float C[][10]);
void sub(float A[][10], float B[][10], float C[][10]);
float d(float A[10][10], int N);
void transpose(float A[10][10], int row, int col);
int main()
{
	int n, r1, c1, r2, c2;
	float A[10][10], B[10][10], p1[10][10], trans[10][10], s1[10][10], m1[10][10], determinant = 0.0, inv[10][10];

	cout << "Enter the number of square matrices [should be >= 1 and <= 2 : \n";
	cin >> n;
	division:
	if (n == 1)
	{
		cout << "\nEnter number of rows and columns of matrix A : \n";
		cin >> r1 >> c1;
		cout << "\n" << "In the form 1 2 3 4 5 6 7 8 9... rows arrange: \n \n";

		cout << "\n Enter the elements of matrix A \n";
		for (int i = 0; i < r1; i++)
		{
			for (int j = 0; j < c1; j++)
			{
				cin >> A[i][j];
			}
		}
		cout << "\n Matrix A is: \n";
		for (int i = 0; i < r1; i++)
		{
			cout << "\n";
			for (int j = 0; j < c1; j++)
			{
				cout << A[i][j] << "\t";
			}
			cout << endl;
		}
	}
	else if (n == 2)
	{
		cout << "\nEnter number of rows and columns of matrix A : \n";
		cin >> r1 >> c1;
		cout << "\nEnter number of rows and columns of matrix B : \n";
		cin >> r2 >> c2;
		cout << "\n" << "In the form 1 2 3 4 5 6 7 8 9... rows arrange: \n \n";
		cout << " Enter the elements of matrix A \n";
		for (int i = 0; i < r1; i++)
		{
			for (int j = 0; j < c1; j++)
			{
				cin >> A[i][j];
			}
		}
		cout << "\n Matrix A is: \n";
		for (int i = 0; i < r1; i++)
		{
			cout << "\n";
			for (int j = 0; j < c1; j++)
			{
				cout << A[i][j] << "\t";
			}
			cout << endl;
		}
		cout << "\n Enter the elements of matrix B \n";
		for (int i = 0; i < r2; i++)
		{
			for (int j = 0; j < c2; j++)
			{
				cin >> B[i][j];
			}
		}
		cout << "\n Matrix B is: \n";
		for (int i = 0; i < r2; i++)
		{
			cout << "\n";
			for (int j = 0; j < c2; j++)
			{
				cout << B[i][j] << "\t";
			}
			cout << endl;
		}

	}

	else
	{
		cout << "\n Number of matrices should be 1 or 2 \n";
	}

	string v;
LOOP: cout << "\nIf you want to quite the program write 'exit' if you want to run press 1 \n";
	cin >> v;
	if (v == "exit")
	{
		return 0;
	}
	else
	{
		int v = 1;
		int s = 0;
		while (v != s)
		{
			int x;
			cout << "\nFor showing the matrix value press 1 \nFor addition press 2 \nFor subtraction press 3 \nFor transpose press 4 \nFor Multiplying press 5 \nFor division press 6 \n";
			cin >> x;
			switch (x)
			{
			case 1:
				if (n == 1)
				{
					cout << "\nThe value of matrix A = \n" << d(A, r1);
				}
				else
				{
					int e;
					cout << "\nFor the value of A press 1 \nFor the value of B press 2 \n";
					cin >> e;
					switch (e)
					{
					case 1:
						cout << "\nThe value of matrix A = \n" << d(A, r1);
						break;
					case 2:
						cout << "\nThe value of matrix B = \n" << d(B, r2);
						break;
					default:
						cout << "\nThe number should be 1 or 2";
						break;
					}
				}
				break;
			case 2:
				if (n == 1)
				{
					add(A, A, p1);
					cout << "\n" << "The sum of matrix A and A is: \n";
					for (int i = 0; i < r1; i++)
					{
						cout << "\n";
						for (int j = 0; j < c1; j++)
							cout << p1[i][j] << "\t";
						cout << endl;
					}
				}
				else {
					int y;
					cout << "\nFor A+A press 1 \nFor B+B press 2 \nFor A+B press 3 \n";
					cin >> y;
					switch (y)
					{
					case 1:
						add(A, A, p1);
						cout << "\n" << "The sum of matrix A and A is: \n";
						for (int i = 0; i < r1; i++)
						{
							cout << "\n";
							for (int j = 0; j < c1; j++)
								cout << p1[i][j] << "\t";
							cout << endl;
						}
						break;
					case 2:
						add(B, B, p1);
						cout << "\n" << "The sum of matrix B and B is: \n";
						for (int i = 0; i < r2; i++)
						{
							cout << "\n";
							for (int j = 0; j < c2; j++)
								cout << p1[i][j] << "\t";
							cout << endl;
						}
						break;
					case 3:
						add(A, B, p1);
						cout << "\n" << "The sum of matrix A and B is: \n";
						for (int i = 0; i < r1; i++)
						{
							cout << "\n";
							for (int j = 0; j < c1; j++)
								cout << p1[i][j] << "\t";
							cout << endl;
						}
						break;
					default:
						cout << "\n numbers should be between 1 and 3 \n";
						break;
					}
				}
				break;
			case 3:
			{
				if (n == 1)
				{
					sub(A, A, s1);
					cout << "\n" << "The subtraction of matrix A and A is: \n";
					for (int i = 0; i < r1; i++)
					{
						cout << "\n";
						for (int j = 0; j < c1; j++)
							cout << s1[i][j] << "\t";
						cout << endl;
					}
				}
				else
				{
					int y;
					cout << "\nFor A-A and B-B press 1 \nFor B-A press 2 \nFor A-B press 3 \n";
					cin >> y;
					switch (y)
					{
					case 1:
						sub(A, A, s1);
						cout << "\n" << "The subtraction of matrix A and A or B and B is: \n";
						for (int i = 0; i < r1; i++)
						{
							cout << "\n";
							for (int j = 0; j < c1; j++)
								cout << s1[i][j] << "\t";
							cout << endl;
						}
						break;
					case 2:
						sub(B, A, s1);
						cout << "\n" << "The subtraction of matrix B and A is: \n";
						for (int i = 0; i < r2; i++)
						{
							cout << "\n";
							for (int j = 0; j < c2; j++)
								cout << s1[i][j] << "\t";
							cout << endl;
						}
						break;
					case 3:
						sub(A, B, s1);
						cout << "\n" << "The subtraction of matrix A and B is: \n";
						for (int i = 0; i < r1; i++)
						{
							cout << "\n";
							for (int j = 0; j < c1; j++)
								cout << s1[i][j] << "\t";
							cout << endl;
						}
						break;
					default:
						cout << "\n numbers should be between 1 and 3 \n";
						break;
					}
				}
			}
			break;
			case 4:
				if (n == 1)
				{
					cout << "\nTranspose of Matrix A: \n";
					transpose(A, r1, c1);
				}
				else
				{
					int z;
					cout << "\nFor transpose of A press 1 \nFor B press 2 \n";
					cin >> z;
					switch (z)
					{
					case 1:
						cout << "\nTranspose of Matrix A: \n";
						transpose(A, r1, c1);
						break;
					case 2:
						cout << "\nTranspose of Matrix B: \n";
						transpose(B, r2, c2);
						break;

					default:
						cout << "\n numbers should be between 1 or 2 \n";
						break;
					}
				}
				break;
			case 5:
				if (n == 1)
				{
					for (int i = 0; i < r1; i++)
					{
						for (int j = 0; j < c1; j++)
						{
							m1[i][j] = 0;
							for (int k = 0; k < r1; k++)
							{
								m1[i][j] += A[i][k] * A[k][j];
							}
						}
					}
					cout << "\nProduct of matrix A and A is: \n";
					for (int i = 0; i < r1; i++)
					{
						cout << "\n";
						for (int j = 0; j < c1; j++)
							cout << m1[i][j] << "\t";
						cout << "\n";
					}
				}
				else
				{
					int w;
					cout << "\nFor AxA press 1 \nFor BxB press 2 \nFor AxB press 3 \n";
					cin >> w;
					switch (w)
					{
					case 1:
						for (int i = 0; i < r1; i++)
						{
							for (int j = 0; j < c1; j++)
							{
								m1[i][j] = 0;
								for (int k = 0; k < r1; k++)
								{
									m1[i][j] += A[i][k] * A[k][j];
								}
							}
						}
						cout << "\nProduct of matrix A and A is: \n";
						for (int i = 0; i < r1; i++)
						{
							cout << "\n";
							for (int j = 0; j < c1; j++)
								cout << m1[i][j] << "\t";
							cout << "\n";
						}
						break;
					case 2:
						for (int i = 0; i < r2; i++)
						{
							for (int j = 0; j < c2; j++)
							{
								m1[i][j] = 0;
								for (int k = 0; k < r2; k++)
								{
									m1[i][j] += B[i][k] * B[k][j];
								}
							}
						}
						cout << "\nProduct of matrix B and B is: \n";
						for (int i = 0; i < r2; i++)
						{
							cout << "\n";
							for (int j = 0; j < c2; j++)
								cout << m1[i][j] << "\t";
							cout << "\n";
						}
						break;
					case 3:
						if (c1 != r2)
						{
							cout << "\nMatrices cannot be multiplied!";
							exit(0);
						}
						else
						{
							for (int i = 0; i < r1; i++)
							{
								for (int j = 0; j < c2; j++)
								{
									m1[i][j] = 0;
									for (int k = 0; k < r2; k++)
									{
										m1[i][j] += A[i][k] * B[k][j];
									}
								}
							}
							cout << "\nProduct of matrices A and B \n";
							for (int i = 0; i < r1; i++)
							{
								cout << "\n";
								for (int j = 0; j < c2; j++)
									cout << m1[i][j] << "\t";
								cout << "\n";
							}
							break;
					default:
						cout << "\n numbers should be between 1 and 3 \n";
						break;
						}
					}
				}
				break;
			case 6:
				cout << "\nTo make division the matrix must be 3x3";
				if (r1&c1 == 3)
				{
					if (n == 1)
					{
						for (int i = 0; i < r1; i++)
							determinant = determinant + (A[0][i] * (A[1][(i + 1) % 3] * A[2][(i + 2) % 3] - A[1][(i + 2) % 3] * A[2][(i + 1) % 3]));

						for (int i = 0; i < r1; i++)
						{
							for (int j = 0; j < c1; j++)
							{
								inv[i][j] = ((A[(j + 1) % c1][(i + 1) % c1] * A[(j + 2) % c1][(i + 2) % c1]) - (A[(j + 1) % c1][(i + 2) % c1] * A[(j + 2) % c1][(i + 1) % c1])) / determinant;

							}
						}
						for (int i = 0; i < r1; i++)
						{
							for (int j = 0; j < c1; j++)
							{
								m1[i][j] = 0;
								for (int k = 0; k < r1; k++)
								{
									m1[i][j] += A[i][k] * inv[k][j];
								}
							}
						}
						cout << "\nDivision of matrices A and A\n";
						for (int i = 0; i < r1; i++)
						{
							cout << "\n";
							for (int j = 0; j < c1; j++)
								cout << m1[i][j] << "\t";
							cout << "\n";
						}
					}
					else {
						int o;
						cout << "\nFor A/A or B/B press 1 \nFor A/B press 2 \nFor B/A press 3 \n";
						cin >> o;
						switch (o)
						{
						case 1:
							for (int i = 0; i < r1; i++)
								determinant = determinant + (A[0][i] * (A[1][(i + 1) % 3] * A[2][(i + 2) % 3] - A[1][(i + 2) % 3] * A[2][(i + 1) % 3]));

							for (int i = 0; i < r1; i++)
							{
								for (int j = 0; j < c1; j++)
								{
									inv[i][j] = ((A[(j + 1) % c1][(i + 1) % c1] * A[(j + 2) % c1][(i + 2) % c1]) - (A[(j + 1) % c1][(i + 2) % c1] * A[(j + 2) % c1][(i + 1) % c1])) / determinant;

								}

							}
							for (int i = 0; i < r1; i++)
							{
								for (int j = 0; j < c2; j++)
								{
									m1[i][j] = 0;
									for (int k = 0; k < r1; k++)
									{
										m1[i][j] += A[i][k] * inv[k][j];
									}
								}
							}
							cout << "\nDivision of matrices A and A or B and B\n";
							for (int i = 0; i < r1; i++)
							{
								cout << "\n";
								for (int j = 0; j < c1; j++)
									cout << m1[i][j] << "\t";
								cout << "\n";
							}
							break;
						case 2:
							for (int i = 0; i < r2; i++)
								determinant = determinant + (B[0][i] * (B[1][(i + 1) % 3] * B[2][(i + 2) % 3] - B[1][(i + 2) % 3] * B[2][(i + 1) % 3]));


							for (int i = 0; i < r2; i++)
							{
								for (int j = 0; j < c2; j++)
								{
									inv[i][j] = ((B[(j + 1) % c2][(i + 1) % c2] * B[(j + 2) % c2][(i + 2) % c2]) - (B[(j + 1) % c2][(i + 2) % c2] * B[(j + 2) % c2][(i + 1) % c2])) / determinant;

								}

							}
							for (int i = 0; i < r1; i++)
							{
								for (int j = 0; j < c2; j++)
								{
									m1[i][j] = 0;
									for (int k = 0; k < r2; k++)
									{
										m1[i][j] += A[i][k] * inv[k][j];
									}
								}
							}
							cout << "\nDivision of matrices A and B\n";
							for (int i = 0; i < r1; i++)
							{
								cout << "\n";
								for (int j = 0; j < c2; j++)
									cout << m1[i][j] << "\t";
								cout << "\n";
							}
							break;
						case 3:
							for (int i = 0; i < r1; i++)
								determinant = determinant + (A[0][i] * (A[1][(i + 1) % 3] * A[2][(i + 2) % 3] - A[1][(i + 2) % 3] * A[2][(i + 1) % 3]));


							for (int i = 0; i < r1; i++)
							{
								for (int j = 0; j < c1; j++)
								{
									inv[i][j] = ((A[(j + 1) % c1][(i + 1) % c1] * A[(j + 2) % c1][(i + 2) % c1]) - (A[(j + 1) % c1][(i + 2) % c1] * A[(j + 2) % c1][(i + 1) % c1])) / determinant;

								}

							}
							for (int i = 0; i < r2; i++)
							{
								for (int j = 0; j < c1; j++)
								{
									m1[i][j] = 0;
									for (int k = 0; k < r1; k++)
									{
										m1[i][j] += B[i][k] * inv[k][j];
									}
								}
							}
							cout << "\nDivision of matrices B and A\n";
							for (int i = 0; i < r2; i++)
							{
								cout << "\n";
								for (int j = 0; j < c1; j++)
									cout << m1[i][j] << "\t";
								cout << "\n";
							}
							break;
						default:
							cout << "\nNumber should be 1 or 2 or 3\n";
							break;
						}
					}
				}
				else
				{
				goto division;
 }
				break;

			default:
				cout << "\n numbers should be between 1 and 6 \n";
				break;
			}
			goto LOOP;
		}
	}
}
void add(float A[][10], float B[][10], float C[][10])
{
	int i, j;
	for (i = 0; i < 10; i++)
	{
		for (j = 0; j < 10; j++)
		{
			C[i][j] = A[i][j] + B[i][j];
		}
	}
}
void sub(float A[][10], float B[][10], float C[][10])
{
	int i, j;
	for (i = 0; i < 10; i++)
	{
		for (j = 0; j < 10; j++)
			C[i][j] = A[i][j] - B[i][j];
	}
}
void transpose(float A[10][10], int row, int col)
{
	float trans[10][10];
	for (int i = 0; i < 10; i++)
	{
		for (int j = 0; j < 10; j++)
		{
			trans[j][i] = A[i][j];
		}
	}
	for (int i = 0; i < row; i++)
	{
		cout << "\n";
		for (int j = 0; j < col; j++)
		{
			cout << trans[i][j] << "\t";
		}
		cout << endl;

	}

}
float d(float A[10][10], int N)
{
	int i, i1, j, j1, x;
	float R[10][10], det = 0;
	if (N == 1) {
		return A[0][0];
	}
	else if (N == 2) {
		return A[0][0] * A[1][1] - A[1][0] * A[0][1];
	}
	else {
		for (x = 0; x < N; x++) {
			i1 = 0;
			for (i = 1; i < N; i++) {
				j1 = 0;

				for (j = 0; j < N; j++) {
					if (j == x) {
						continue;
					}
					R[i1][j1] = A[i][j];
					j1++;

				}
				i1++;
			}
			det += (pow(-1, x) * A[0][x] * d(R, N - 1));
		}
	}
	return det;
}
