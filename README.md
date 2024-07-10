# Solidity Take Home Assessment

You are required to develop the smart contracts and test files for a lending protocol. You must clone this repository to one of your own private repo's and add your assessors as reviewers.

Please use foundry as your environment.

# Task Overview

You are required to develop a lending protocol which uses a credit rating system as a form of collateral. In most lending protocols, users are required to over collateralize their assets due to the anonymous nature of users on the blockchain. As this works for now, we know it is not a long term solution and we need to provide ways for users to borrow funds without over having to over collateralize. One way is to build a credit system where user addresses are associated with a credit score. In a perfect world, this credit score would be an accumulation of all the users activity throughout multiple protocols. However, for the simplicity of this assignment, users credit score will be native to only this protocol.

# In depth requirements

We would like to leave many of the options open for your creativity and architectural skills. However, their are a few key features the protocol needs to be built around. The primary function of the protocol is to allow lenders and borrowers to interact seamlessly without the need for any intermediaries. The protocol will only handle USDC, ETH and MATIC. Lenders will be able to deposit any of these three assets in return for our internal tokens which act as shares. Our internal tokens will be saUSDC, saETH and saMATIC. At any point, the lenders should be able to redeem their protocol tokens for the respective amount of assets back.

Lenders will only contribute funds into our protocol if they can receive interest on their deposits. Therefore, our tokens will rebase as more borrowers pay interest. This means if you lend a token which is of higher priority to borrowers, you receive a higher APY.

The other side of the protocol are the borrowers. Users should be able to borrow either USDC, ETH or MATIC and pay back their funds with small margins of interest. A borrower will need to provide collateral in replace for the funds they are borrowing to ensure they do not run off with the funds. However, we will have an internal credit rating where borrowers provide collateral based on their credit score (It is important to note that an internal, protocol based, credit system is not good practice in the real world and is only used to keep this assignment simple). The credit system is left entirely up to your imagination. Just ensure that users who act good and pay on time increase their credit score and in return, pay less collateral AND interest on future borrows. Users who pay late or do not lay at all should either be blacklisted or required to pay higher interest rates and more collateral on future borrows.

# Minimum Viable Product due for assignment

This is a large task and in the real world would require weeks of planning and development. We do not expect you to develop this system in full. We would like to assess how far you get in the provided deadline and the quality of code you provide. With that said, there are a few MVP features we require to be complete by the deadline. These are:

Token contracts for saUSDC, saETH and saMATIC
Functionality for a lender to deposit USDC, ETH and MATIC and receive saUSDC, saETH and saMATIC in return.
Functionality for a lender to redeem their saUSDC, saETH and saMATIC for USDC, ETH and MATIC in return. Receiving yields due to the token rebasing.
Tests to cover all the above functionality.
Functionality around borrowers and their credit score is not needed currently but may be asked for you to build in the future if we feel we need more code to examine.

The MVP for the assignment is focused on building a seamless lending facility where users with funds can deposit their assets to achieve high APYs.

# Testing

With regards to testing. We would like to see as close to 100% test coverage as possible. When testing the lenders yield returns, you may just deposit funds into the contracts to trigger the rebase. In the real protocol, as borrowers pay interest, and the balance of the assets increase, the tokens rebase. Therefore, because you are not building the borrowing section of the protocol, you can simulate interest by depositing funds into the contract in the unit tests.
