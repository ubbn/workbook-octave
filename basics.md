
**Basic commands**  
```format short```		- short format for long decimal number  
```format long```		- shows long decimal number  
  
```~=```				not equal !=  
```or(a,b)```			boolean OR operation  
```xor(a,b)```		boolean XOR  
```disp(a)```			prints only value of variable a  
```sprintf('%0.2f', -3.666)```		print value with given precision in string  
```%```				comment  
  
  
**Matrix operation**  
```a=[3 23; 3 2; 4 5]```	- 3x2 matrix declaration  
```b=start:end```			create row matrix from start till end incrementing by 1  
```c=start:step:end```	create row matrix first number start with each step till end  
```Magic(n)```			% return matrix filled with 1 - nxn numbers unique, sum of each col/row is equal  
```Zeros(n,m)```			% generates nxm size of matrix full of zeros  
```Ones(n,m)```			% generates nxm size of matrix full of ones  
```Rand(n)``` 		% generate random matrix of nxn size  
```Eye(n)```				% generate index matrix of nxn size  
  
  
**Computing Data**  
A * B		multiply A matrix with B  
A .* B		multiply A matrix with B each corresponding element-wise  
A .^ 2		element-wise square of each element  
A + n	% element wise add number n to each element  
1 ./ B	% print inverse of B matrix  
A’		% transpose of B matrix  
A < 3	% print same size of A matrix filled with 1/0 element-wise comparison with the number  
Max(A)	% print max element of each column (default)  
Prod(A)	% print product of multiplication of all elements of A matrix  
Pinv(A)	% print pseudo-inverse of matrix A  
Sum(A)	% print sum of all elements of A matrix  
Sum(A,1)		% print sum of each column’s all elements of A matrix  
Sum(A,2)		% print sum of each row’s all elements of A matrix  
Find(a<3)	% prints positions of elements of a which less than the number  
sqrt(n)		% get square root of N  
floor(a)		round down values of each matrix element  
  
  
**Data manipulation**  
A(i : end)		% Serialize elements from index i till endN into row vector  
A(i : j)		% Serialize elements from index i till index j into row vector  
A(i, :)		% Select i-th row with its all columns  
A([i, j], :)		% Select i and j-th rows with all columns  
A(i : j, :)		% Select part from row i till row j including all columns  
A(i : j, k:m)	% Select part from row i till row j including from column k till column m  
[A, [i; j; ...]]	% Append column vector to A matrix  
A(:)			% Put all dimensions elements into single vector  
[A B]		% Combine matrices of A and B in column  
[A; B]		% Combine matrices of A and B in row  
  
**Plot data**  
```hist(w)```		% show histogram of give function w  
  
```x=[0:0.01:0.98]```	% defines argument range (x axis)  
```y1 = sin(2*pi*x);```	% defines a function  
```y2 = cos(2*pi*x);```	% defines a function  
```plot(x, y1)```		% plot function with given range of parameter  
```hold on```			% plots after it will be drawn on same board  
```plot(x, y2, 'r')```		% plot function with color red  
```xlabel('time')```		% set label for x axis  
```ylabel('value')```		% set label for y  
```legend('sin', cos)```	% put legend/remark for each graph  
```title('Title of graph')```  
```print -dpng 'MyPlot.png'```		% export plot to image  
```close```			% close plot  
  
size(a)		size/all dimension of matrix  
size(a, n)		size n-th dimension (1 - row, 2 - column ... )  
length(a)		gives size of longest dimension X or Y  
  
  
```who```			all variables  
```whos```		more details about variables  
```clear a```		clear variable a  
```clear```		clears all varuables  
  
  
**File handling**  
```save <filename> <variable> -ascii```		% save variable data to file (optionally in ascii format)  
```load <filename>```						% load data from a file  
  
**Control statements**  
* For loop  
```octave
v=zeros(10,1)  
for i=1:10,  
	v(i) = 2 ^ i;  
end;  
```  
  
* while loop  
```octave
i = 1,  
while i <= 5,  
	v(i) = i;  
	i = i + 1;  
end;  
```  

```break;```		% Control commands in loops  
```continue;```  

```octave
if v(i) == 1,
	disp('One')
elseif v(i) == 2
	disp('Two')
else
	disp('Other')
end
```

**Function**  
Octave searches functions from current dir and its listed path  
Octave function can return multiples values  
```octave
function y = squareThisNumber(x)  
	y = x ^ 2;  

squareThisNumber(4);  

function [y1, y2] = 	squareAndCubeThisNumber(x)
	y1 = x ^ 2;
	y2 = x ^ 3;

[a, b] = function(5);
```


Vectorization
Optimization method on Octave





