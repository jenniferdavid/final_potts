Final-potts
============
You need [Eigen][] v3.

After cloning the repository, open a terminal

    git clone https://github.com/jenniferdavid/final-potts.git final-potts
    mkdir final-potts/OUTPUTS
    gedit final_potts.cpp
    g++ -pg -o final_potts -std=c++11 final_potts.cpp -I /usr/local/include/eigen3 -lboost_iostreams -lboost_system -lboost_filesystem
    ./final_potts M N kT_start kT_end kT_fac gamma -read -exact -default -random eta Tkappa -max

open the cpp file to change the input and output paths (line nos 104 and 105)

M -> no of vehicles

N -> no of tasks

kT_start -> start temperature

kT_end -> end temperature

kT_fac -> kT_step temperature

gamma -> Loop function weighing factor

-read or -random -> reads input data / generates random data based on normal distribution

-exact or -iterative or -SM -> Updating PMatrix

-default or -trace -> Eloop function calculation either using Yij or trace

-random or -optimal -> random for default method, optimal is the hybrid method (takes the optimal solution as initial Vs)

eta -> Normalisation function weighing factor

Tkappa -> Cost function weighing factor

-max or -sum -> Using sum or max function

[Eigen]: http://eigen.tuxfamily.org/

