# PING testnet
# PING 1 PING TEST PING TEST

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

# PING MAINNET
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Ping {
    mapping(address => bool) public hasPinged;
    uint256 public uniquePingers;

    event Pinged(address indexed pinger, uint256 newCount);

    function ping() external {
        require(!hasPinged[msg.sender], "Already pinged");
        hasPinged[msg.sender] = true;
        uniquePingers += 1;
        emit Pinged(msg.sender, uniquePingers);
    }
}

Check it out

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Ping {
    mapping(address => bool) public hasPinged;
    uint256 public uniquePingers;

    event Pinged(address indexed pinger, uint256 newCount);

    function ping() external {
        require(!hasPinged[msg.sender], "Already pinged");
        hasPinged[msg.sender] = true;
        uniquePingers += 1;
        emit Pinged(msg.sender, uniquePingers);
    }
}

PING PING

TEST PING
