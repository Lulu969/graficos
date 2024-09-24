% Definimos la matriz AA y el vector bb
AA = [1.0001 1.0000; 1.0000 1.0000];
bb = [2; 2];

% Creamos una malla de valores para la gráfica
x = linspace(0, 3, 100);
y1 = (bb(1) - AA(1,1)*x) / AA(1,2);
y2 = (bb(2) - AA(2,1)*x) / AA(2,2);

% Crear una nueva ventana de gráficos
figure;

% Graficamos las dos rectas
plot(x, y1, 'r', 'LineWidth', 2); % Primera ecuación
hold on;
plot(x, y2, 'b', 'LineWidth', 2); % Segunda ecuación

% Añadimos etiquetas y título
xlabel('x');
ylabel('y');
title('Gráfico del sistema de ecuaciones');
legend('Ecuación 1', 'Ecuación 2');

% Establecemos el rango de los ejes
axis([0 3 0 3]);

grid on;
hold off;

% Visualización interactiva (activar la ventana de gráficos)
shg;
