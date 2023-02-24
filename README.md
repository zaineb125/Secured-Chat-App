# secured-chat-app
##  A chat application with end-to-end encryption 
This app was built in **python** using TKinter & based on Sockets and the encryption was made with the **RSA** protocol implemented by the [cryptography](https://cryptography.io/en/latest/) library
## the flow 
when you create a new client by signup or login it generates a public and private RSA keys when it connects to the server they exchange public keys
once it's connected the client can send 2 types of messages :
- to specific person : the client encrypts the message and the receiver with the server public key then the server decrypts it to extract the receiver and encrypt the rest with the receiver's public key and send it
- to everyone : the client encrypts the message with the server public key then the server decrypts it and broadcast it while encrypting it with each client public key before sending
#### before starting you need to run these commands to install necessary packages :
```
pip install --upgrade Pillow
pip install cryptography
```
#### to start you need to run the server first :
```
python server.py
```
#### then run signup.py to create some clients to communicate (or login.py if you have already an account) 
```
python signup.py
```

<h1> Some photos to illustrate the work </h1>


<h2> 1)SignUp : </h2>
<br/>
<img height="70%" width="70%" src="https://user-images.githubusercontent.com/56805500/221287246-c6821e2e-429c-4030-a5d6-5a31f91b0112.png" alt="sign-up"/>
<br/>
The user will get an error if the userName does exist :
<br/>
<img height="70%" width="70%" src="https://user-images.githubusercontent.com/56805500/221287724-45bc642f-9a07-4875-b001-c84c9b3677bc.png" alt="sign-up"/>
<br/>
<br/>
<p> else the user is successfully signed up . </p>
<br/>
<br/>
<h2> 2)Start the chat between connected users : </h2> 
<br/>
<img height="70%" width="70%" src="https://user-images.githubusercontent.com/56805500/221288007-a90f19e5-d102-45d8-8174-0682336d57b9.png" alt="sign-up"/>
<br/>
<br/>
<img height="70%" width="70%" src="https://user-images.githubusercontent.com/56805500/221288026-52e55ca6-2e69-4de1-830f-31c0783fd5fa.png" alt="sign-up"/>
<br/>

