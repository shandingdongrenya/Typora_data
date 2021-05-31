# 三维函数图

```mtalab
%%
clear all; clc;
%---------------------------------------
t = 0 : pi /100 : 2 * pi;
x = 8 * cos(t);
y = 4 * sqrt(2) * sin(t);
z = -4 * sqrt(2) * sin(t);
plot3(x, y, z);
text(0, 0, 0, 'Origin');
grid on;

%---------------------------------------
x = 0 : 0.1 : 2 * pi;
y = 0 : 0.1 : 2 * pi;
[X, Y] = meshgrid(x, y); % 生成X-Y平面网格坐标矩阵
Z = cos(X) .* sin(Y); % 生成高度矩阵
figure(1); plot3(X, Y, Z); %画三维网格曲面
title('plot3'); xlabel('x'); ylabel('y'); zlabel('z');

figure(2); mesh(X, Y, Z); %画三维网格曲面
title('mesh'); xlabel('x'); ylabel('y'); zlabel('z');

figure(3); surf(X, Y, Z); %画三维网格曲面
title('surf'); xlabel('x'); ylabel('y'); zlabel('z');

%-----------------------------------------------------
[X, Y, Z] = sphere(50);
subplot(1, 4, 1); surf(X, Y, Z);

[X, Y, Z] = cylinder(50, 50);
subplot(1, 4, 2); surf(X, Y, Z);

t = 0 : pi / 100 : 2 * pi;
[X, Y, Z] = cylinder(2 + sin(t), 50);
subplot(1, 4, 3); surf(X, Y, Z);

[X, Y] = meshgrid(-5 : 0.1 : 5);
Z = peaks(X, Y);
subplot(1, 4, 4); surf(X, Y, Z);

% ----------------------------------------
A = [1, 2, 3; 4, 6, 7];
subplot(2, 2, 1); bar3(A);
xlabel('x'); ylabel('y'); zlabel('z');

subplot(2, 2, 2); stem3(A);
xlabel('x'); ylabel('y'); zlabel('z');

A = [0.1, 0.2, 0.3, 0.25, 0.15];
subplot(2, 2, 3); pie3(A);

subplot(2, 2, 4); fill3(rand(3, 5), rand(3, 5), rand(3, 5), 'b');

% --------------------------------------------------------------------
[X, Y, Z] = peaks(30);
subplot(1, 3, 1); waterfall(X, Y, Z);
title('waterfall'); xlabel('x'); ylabel('y'); zlabel('z');

subplot(1, 3, 2); contour(X, Y, Z, 12); %12为高度等级数
title('2D-contour'); xlabel('x'); ylabel('y');

subplot(1, 3, 3); contour3(X, Y, Z, 12);
title('3D-contour'); xlabel('x'); ylabel('y'); zlabel('z');

%-----------------------------------------------------------
[X, Y, Z] = peaks(30);
subplot(1, 3, 1); waterfall(X, Y, Z);
view(-37.5, 30); %设置图形观看视点(方位角, 仰角)
title('az = -37.5, el = 30'); xlabel('x'); ylabel('y'); zlabel('z');

subplot(1, 3, 2); waterfall(X, Y, Z);
view(0, 30);
title('az = 0, el = 30'); xlabel('x'); ylabel('y'); zlabel('z');

subplot(1, 3, 3); waterfall(X, Y, Z);
view(30, 30);
title('az = 30, el = 30'); xlabel('x'); ylabel('y'); zlabel('z');

```

