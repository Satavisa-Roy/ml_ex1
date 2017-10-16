function J = computeCost(X, y, theta)
%COMPUTECOST Compute cost for linear regression
%   J = COMPUTECOST(X, y, theta) computes the cost of using theta as the
%   parameter for linear regression to fit the data points in X and y

data=load('ex1data1.txt');
y=data(:,2);
m = length(y);
X=[ones(m,1),data(:,1)];
theta=zeros(2,1);
% Initialize some useful values

% number of training examples

% You need to return the following variables correctly 
J = 0;

% ====================== YOUR CODE HERE ======================
% Instructions: Compute the cost of a particular choice of theta
%               You should set J to the cost.

h=X*theta;
sqrErrors=(h-y).^2;
J=[sum(sqrErrors)]/(2*m);

% =========================================================================

end
