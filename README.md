# Blockchain_project
 Blockchain_project
 
 Prerrequisites:
 a) Have Python 3.8 or higher version installed
 b) Have pip installed 
 c) Have Docker app and an account created
 d) Have Metamask account
 
 1.- Create a virtual environment for your project with the command (check firts how to create a virtual environment for your operating system)
 
 python -m venv env 
 
 2.- Install the dependencies from the requirements.txt file with the next command:
 
 python -m pip install -r requirements.txt
 
3.- Create a Ducker image:

docker build -t erick1988/blockchain_x21176221:ecr20 . 

4.- Run the image

docker run -p 8090:8080 --name ecr20_block_harbor -d erick1988/blockchain_x21176221:ecr20

docker run -p 8090:8080 --name x21176221 -d erick1988/blockchain_x21176221:ecr20

docker build -t erick1988/blockchain_x21176221:ecr20 .
 
 
 5.- Run the next command to transfer some Ether:
 
 curl --header "Content-Type: application/json" --request POST --data '{"address":"0x42442147D273EaC997EA77217C9E5C170434FF7D","amount":"0.005"}' http://localhost:8090/eth
 
 Note: you have to change the address for the one you want to transfer Ether and also change the amount for the desired one
 
 6.- Run the next command to transfer tokens:

curl --header "Content-Type: application/json" --request POST --data '{"address":"0x42442147D273EaC997EA77217C9E5C170434FF7D"}' http://localhost:8090/token

Note: change the address for the one you want to send tokens
