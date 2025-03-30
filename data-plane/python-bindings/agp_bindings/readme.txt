# follow this sequence
python agpserver.py 

# set agpclient2 to LISTEN what message is sent to it by agpclient1
python agpclient2.py -l "org1/ns1/agent2" -g "http://127.0.0.1:46357" 

# send a message from agent1 in agpclient1. the message is "Hello from agent1\!
python agpclient1.py -l "org1/ns1/agent1" -r "org1/ns1/agent2" -m "Hello from agent1\!" -g "http://127.0.0.1:46357" -i 1

# ----works fine