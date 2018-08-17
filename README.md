# rustchain
A simple blockchain in rust

## guide
Startup rustchain by running `cargo run` in this directory. Once it starts up a webserver will open at localhost:3000. There are 3 requests that can be sent to the blockchain:

### GET /chain
This returns a json array of the blockchain to date

### GET /mine
This mines the chain

## POST /transactions/new

{
  "sender" : "address",
  "recipient" : "address",
  "amount" : 25
}

Sending a request with the body in the form above (in raw text json) will push a new transaction onto the chain. It will be mined into the chain the next time you call /mine
