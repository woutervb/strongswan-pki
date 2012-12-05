Introduction
============
 
These small scripts are meant for simple pki management
 
The function of the scripts is:
  1. Create a CA
  2. Create a strongswan server certificate, compatible with windows 7 and OSX (to be tested)
  3. Create client certificates for the CA created in 1
 

Basic usage
===========
 
    ./1-self_sign_ca
    This will create a CA, change the script to contain YOUR details
 
    ./2-create_gateway_cert <dns name of the strongswan gateway>
    Will create a gateway (server) certificate, containing the required flags
    for windows 7 and mac OS X. This has (not) been tested.
    This certificate will be signed by 1
 
    ./3-create_peer_cert <peer name>
    Will create peer certificated and wrap them in a nice pkcs12 container,
    containing the complete chain.
    This certificate will be signed by 1
