# Solidity Take Home Assessment

You are required to build a simple escrow contract which faciliates a simple gambling game.

Please use Foundry as your development environment.

Please add @garethjameslarkan and @saksijas to your repo for review.

# Task Overview

We would like to faciliate a simple gambling game, where two users compete by betting on the ETH/USDC price. Two users will go head to head by deciding what will come first, an increase of the ETH price by 5% or a decrease of the ETH price by 5%. If at any point, one of these barriers are reached, the winning player can call closeGame and the escrow contract should verify they have won and send the entry fees to the winner.

# Minimum Viable Product due for assignment

Escrow contract with the following functionality: 
  - Entry into game for first player ($1000 USDC entrance fee) - Chosen selection of increase or decrease
  - Entry into game for second player ($1000 USDC entrance fee) - Must be opposite choice to player 1
  - Entry of second player should only be allowed to happen if the price has not fluctuated by more than 1% from when the original user entered.
  - Withdrawing of entry for first player ONLY if a second player has not entered.
  - Once second player has entered, no one can withdraw
  - Function to closeGame and winner gets sent their funds

# Testing

With regards to testing. We would like to see as close to 100% test coverage as possible. 
