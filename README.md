# Optimal-Reactive-Power-
Optimal Reactive Power Calculation in Power System Using MATPOWER  Codes at each Bus of a Case
define_constants;
Foptimal = fopen (‘f.csv’,’w’);
 B= [4 5 7 10 11 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57]; 
j =8;
for I =1:50
   A=B(i);
   P=200;
mpc=loadcase(‘case57c’);
ng = size(mpc.gen, 1) + 1; 
mpc.bus (A,BUS_TYPE)= 2;    
mpc.gencost(j,MODEL)=2;
mpc.gen(ng, GEN_BUS:PMIN) = [A 0 0 P –P 1 100 1 0 0];
mpc = runopf(mpc);
x=mpc.f;
fprintf(foptimal,’%f %f\n',A,x);
j = j+1;
end
fclose(foptimal);
type('f.csv');
display (foptimal)

