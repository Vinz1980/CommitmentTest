# CommitmentTest
# Commit 1
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.24;

contract Ping {
    event Pinged(address indexed pinger, uint256 count);
    uint256 public totalPings;

    function ping() external {
        totalPings += 1;
        emit Pinged(msg.sender, totalPings);
    }
}

Hardhat
