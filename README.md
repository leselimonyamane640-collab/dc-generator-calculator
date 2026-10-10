# dc-generator-calculator
DC generator calculations using MATLAB Select Public if you're comfortable sharing the code, check Add a README file, then tap Create repository. Step 2 

% DC_GENERATOR_EMF
% Calculate the generated EMF of a DC generator.
% Formula: Eg = (P * Phi * Z * N) / (60 * A)

clc;
clear;

fprintf('DC GENERATOR EMF CALCULATOR\n');
fprintf('---------------------------\n');

P = input('Enter number of poles, P: ');
Phi = input('Enter flux per pole in webers, Phi: ');
Z = input('Enter total armature conductors, Z: ');
N = input('Enter speed in rpm, N: ');
A = input('Enter number of parallel paths, A: ');

if P <= 0 || Phi <= 0 || Z <= 0 || N <= 0 || A <= 0
    error('All inputs must be greater than zero.');
end

Eg = (P * Phi * Z * N) / (60 * A);

fprintf('\nGenerated EMF, Eg = %.2f V\n', Eg);

% Test example:
% P = 4, Phi = 0.02 Wb, Z = 600
% N = 1000 rpm, A = 4
% Expected result: Eg = 200 V
