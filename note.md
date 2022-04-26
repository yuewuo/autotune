

./ex/bin/ex1 -ems ./ex/ems -d 3 -p 0.01 -t_delete 100 -boot 1 -screen
./ex/bin/ex1 -ems ./ex/ems -d 3 -p 0.01 -t_delete 10000 -boot 1 -screen


./ex/bin/ex1 -ems ./ex/ems -d 3 -p 0.01 -t_check 10000 -t_delete 20000 -screen -max_num_X 100000000 -max_num_Z 100000000


./ex/bin/ex1 -ems ./ex/ems -d 17 -p 0.0065 -screen -verbose -boot 0 -t_check 275

# `t_delete` default to 100, which is enough according to the MANUAL.md
./ex/bin/ex1 -ems ./ex/ems -d 17 -p 0.001 -screen -verbose -boot 0
./ex/bin/ex1 -ems ./ex/ems -d 17 -p 0.001 -screen -verbose -boot 0


... I guess they got d^2 scale because of too small t_delete.... syndromes are deleted before they even match!!!
./ex/bin/ex1 -ems ./ex/ems -d 17 -p 0.001 -screen -verbose -boot 0 -t_check 200 -t_delete 5
./ex/bin/ex1 -ems ./ex/ems -d 17 -p 0.001 -screen -verbose -boot 0 -t_check 200 -t_delete 10
./ex/bin/ex1 -ems ./ex/ems -d 17 -p 0.001 -screen -verbose -boot 0 -t_check 200 -t_delete 100


# now let me keep the same t_delete and use the default boot function to see what happens!
./ex/bin/ex1 -ems ./ex/ems -d 4 -p 0.001 -screen -verbose -boot 1
./ex/bin/ex1 -ems ./ex/ems -d 8 -p 0.001 -screen -verbose -boot 1
./ex/bin/ex1 -ems ./ex/ems -d 16 -p 0.001 -screen -verbose -boot 1
./ex/bin/ex1 -ems ./ex/ems -d 32 -p 0.001 -screen -verbose -boot 1
./ex/bin/ex1 -ems ./ex/ems -d 64 -p 0.001 -screen -verbose -boot 1
./ex/bin/ex1 -ems ./ex/ems -d 128 -p 0.001 -screen -verbose -boot 1

# t_check contributes to a very small amount of time: the mwpm that runs after each round is the major source
./ex/bin/ex1 -ems ./ex/ems -d 64 -p 0.001 -screen -verbose -boot 0 -t_check 100


# reproduce p=0.005, d=7  (my m1-mac is about 2x slower than in paper)
./ex/bin/ex1 -ems ./ex/ems -d 7 -p 0.005 -screen -boot 0 -t_check 88


./ex/bin/ex1 -ems ./ex/ems -d 17 -p 0.005 -screen -boot 0 -t_check 5885 -verbose
