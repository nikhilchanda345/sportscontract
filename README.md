# Sports Contract 

## Overview

This Solidity smart contract, named "SportsContract," facilitates the management of sports event registrations on the Ethereum blockchain. The contract allows an organizer to control the registration status, change the organizer's address, and open/close registration for the sports event.

## Smart Contract Details

### State Variables

- `organizer`: Represents the Ethereum address of the current organizer of the sports event.
- `isRegistrationOpen`: A boolean variable indicating whether event registration is currently open or closed.

### Constructor

- Initializes the `organizer` variable with the address of the contract deployer (presumed to be the initial organizer).
- Sets the `isRegistrationOpen` variable to `true` by default, indicating that registration is initially open.

### Functions

1. **changeOrganizer(address newOrganizer)**
   - Allows the current organizer to transfer ownership to a new address.
   - Requires that the caller is the current organizer.

2. **closeRegistration()**
   - Closes the event registration.
   - Uses `assert` to ensure that registration is open before closing.

3. **openRegistration()**
   - Opens the event registration.
   - Uses `revert` to handle the exceptional case when registration is already open.

## Usage

1. **Deploying the Smart Contract:**
   - Deploy the smart contract to the Ethereum blockchain.

2. **Changing the Organizer:**
   - Call the `changeOrganizer` function to transfer ownership to a new address.
   - Only the current organizer can execute this function.

3. **Closing Registration:**
   - Execute the `closeRegistration` function to close event registration.
   - Ensures that registration is currently open using `assert`.

4. **Opening Registration:**
   - Invoke the `openRegistration` function to open event registration.
   - Handles the case where registration is already open by using `revert`.


## Author

[Nikhil Chandha]
[nikhilchanda098@gmail.com]
