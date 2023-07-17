// Define a smart contract named EthContract
contract EthContract {
    // Declare a variable to store the balance of the contract
    uint256 public balance;

    // Constructor function, called when the contract is deployed
    constructor() payable {
        // Assign the balance of the contract to the amount of ether sent along with the deployment
        balance = msg.value;
    }

    // Withdraw function, allows the sender to withdraw the ether they sent
    function withdraw() public {
        // Check condition: the sender must be the creator of the contract
        require(msg.sender == address(this));
        // Send back the amount of ether equal to the balance of the contract to the sender
        payable(msg.sender).transfer(balance);
        // Reset the balance of the contract to 0
        balance = 0;
    }
}
- 👋 Hi, I’m @Athena-eth
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Athena-eth/Athena-eth is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
