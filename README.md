# Intro-to-Blockchain
# IPFS
# IPFS Practical - Uploading a File to IPFS

## IPFS Installation

I downloaded and installed **IPFS Desktop for Windows** from the official website:  
🔗 [https://docs.ipfs.tech/install/ipfs-desktop/](https://docs.ipfs.tech/install/ipfs-desktop/)

## IPFS Setup

After the installation, I opened the IPFS Desktop application.  
The IPFS node connected automatically, and the status showed as **Online**.

![Screenshot 2025-04-08 161601](https://github.com/user-attachments/assets/20c8981f-cbb8-4a6d-8ff7-026e4df0d58b)

## File Upload

To upload a file:

1. I navigated to the **Files** section within IPFS Desktop.
2. Then, I clicked on the **Import** button.
3. I uploaded a few sample files – including a **SQL Notes**.

Once uploaded, IPFS automatically generated a unique **CID (Content Identifier)** for each file.

 ![Screenshot 2025-04-08 161448](https://github.com/user-attachments/assets/431be20b-f039-49fa-a7a5-0a5262d29bbb)
![Screenshot 2025-04-10 203333](https://github.com/user-attachments/assets/1d5bf6cf-0987-4eec-b86c-6add6c968b84)

# Assignment 5: IPFS Privacy and Encryption
This assignment demonstrates how to use the InterPlanetary File System (IPFS) along with OpenSSL to perform file encryption and ensure privacy via the command line.

# Steps
# 1. Create a file to be added to IPFS
```

echo "Hello, IPFS!" > myfile.txt
```
<br>

# 2.Add the original file to IPFS
```

ipfs add myfile.txt
```
# 3.Encrypt the file using OpenSSL (AES-256-CBC)
```

openssl enc -aes-256-cbc -pbkdf2 -iter 100000 -salt -in myfile.txt -out myfile_encrypted.txt -pass pass:yourpassword
```
# 4.Add the encrypted file to IPFS
```

ipfs add myfile_encrypted.txt
```
# 5.View the encrypted file (optional)
```

cat myfile_encrypted.txt
```
# 6.Decrypt the file
```

openssl enc -d -aes-256-cbc -pbkdf2 -iter 100000 -in myfile_encrypted.txt -out decrypted_file.txt -pass pass:yourpassword
```
# 7.Verify the decrypted file content
```

cat decrypted_file.txt
```
# 8.Add the decrypted file to IPFS
```

ipfs add decrypted_file.txt
```

![Screenshot 2025-05-18 163525](https://github.com/user-attachments/assets/df525435-ef5e-40d8-809b-b6bfbadcd9a2)


# Notes
● Replace `yourpassword` with a strong, secure password of your choice.
<br>
● Ensure that IPFS is properly installed and initialized before running these commands.
# Blockchain Practical - MetaMask Wallet & Sepolia Testnet

This repo contains my blockchain practical work for creating a MetaMask wallet, receiving Sepolia test ETH, and making a transaction on the Sepolia testnet.

---

## 🔐 MetaMask Wallet Creation (Sepolia Testnet)

### Introduction
In this practical, I created a MetaMask wallet and performed a transaction using the Sepolia testnet. This includes setting up MetaMask, connecting to Sepolia, claiming test ETH from the faucet, and sending a transaction.

---

## ✅ Transaction Details

- **Network:** Sepolia Testnet  
- **Amount Sent:** 0.03 ETH  
- **Transaction Hash:**  
`0xe46a19661d6c3cf7f10be37d87a9bcd01152972979132b088ee46f090c164712`  
[🔗 View on Etherscan](https://sepolia.etherscan.io/tx/0xe46a19661d6c3cf7f10be37d87a9bcd01152972979132b088ee46f090c164712)  
- **Status:** Successful ✅

---

## 💸 Getting Sepolia ETH from Faucet

1. Opened the Sepolia Faucet hosted on Google Cloud.
2. Logged in using my Google account.
3. Copied and pasted my MetaMask wallet address into the input field.
4. Clicked on **"Request 0.05 ETH"**.
5. ETH was successfully sent to my wallet in a few seconds.
6. Verified the deposit by checking on Sepolia Etherscan.

### 📸 Screenshot:
Sepolia Faucet transaction request page:
![Screenshot 2025-04-10 193114](https://github.com/user-attachments/assets/269a6f10-90a9-4f2a-8d9a-1176abaf6ad7)

---

## 🔁 Steps Followed for the Transaction

1. Installed MetaMask extension on my browser.
2. Created a new wallet and backed up the Secret Recovery Phrase.
3. Connected MetaMask to **Sepolia Testnet** (added custom network manually).
4. Claimed **test ETH** from the faucet.
5. Sent **0.03 ETH** to another wallet address using MetaMask.
6. Verified transaction success on Sepolia Etherscan.

---

## 📤 Transaction Screenshot

Below is the screenshot showing the transaction confirmation inside MetaMask:

![Screenshot 2025-04-10 193638](https://github.com/user-attachments/assets/9f1f08dd-2f68-4061-9fed-e30bcfc5c2e7)

---

> Created by: *[Himanshu Rao]*  

# Hyperledger-Fabric

## 1. Install Golang  
```bash
sudo apt install golang-go
```
Installs Golang, which is necessary for running Hyperledger Fabric binaries.

## Screenshot 

![Screenshot 2025-04-13 130047](https://github.com/user-attachments/assets/34277b4b-807e-407e-a0a1-15625793b47d)


---

## 2. Check Docker Version  
```bash
docker --version
```
Verifies that Docker is installed and running correctly.

## Screenshot 

![Screenshot 2025-04-13 161049](https://github.com/user-attachments/assets/893cb8a2-050b-434c-9350-4c76be8bb23c)
_

---

## 3. Check Docker Compose Version  
```bash
docker compose version
```
Verifies the installation of Docker Compose.

## Screenshot

![Screenshot 2025-04-13 161201](https://github.com/user-attachments/assets/d6bc63c1-dd15-46f3-a902-04e4dc1d3f41)


---

## 4. List Files in Current Directory  
```bash
ls
```
Shows the list of files and folders in the current directory.

---

## 5. Clone the Fabric Samples Repository and Move into the Cloned Folder  
```bash
git clone https://github.com/fabric-samples.git; cd fabric-samples
```
Downloads the official Hyperledger Fabric sample code from GitHub.  
Enters the cloned folder where Fabric examples are available.

## Screenshot 

![Screenshot 2025-04-13 161348](https://github.com/user-attachments/assets/997a447c-38f7-44c0-b18b-5bb380382f24)


---

## 6. Download Fabric Binaries  
```bash
curl -sSL https://bit.ly/2ysbOFE | bash -s
```
Downloads necessary Fabric binaries and Docker images like peer, orderer, and cryptogen.

## Screenshot

![Screenshot 2025-04-13 163554](https://github.com/user-attachments/assets/603a1a43-1e3f-44fb-bc62-f5e0691a3e10)
![Screenshot 2025-04-13 171636](https://github.com/user-attachments/assets/a2642bf3-6a0f-4a9f-9df1-ad7fc2f5d3a5)
![Screenshot 2025-04-13 171730](https://github.com/user-attachments/assets/b9f5863c-e5e5-4ebf-8135-b972c148974c)
![Screenshot 2025-04-13 171749](https://github.com/user-attachments/assets/7cdb4657-5e46-47dc-97be-b61009d92d27)


---

## 7. Enter the Test Network Directory  
```bash
cd test-network
```
Navigates to the directory that contains scripts for running a sample Fabric network.

## Screenshot

![Screenshot 2025-04-13 163740](https://github.com/user-attachments/assets/948647e5-a691-4031-ba2f-efdccd197549)


---

## 8. View the Network Script  
```bash
./network.sh
```
Shows the options available with the `network.sh` script.

## Screenshot

![Screenshot 2025-04-13 172111](https://github.com/user-attachments/assets/bf6836bf-87e9-4daa-a4cb-a4ea6eafa4c4)
![Screenshot 2025-04-13 172147](https://github.com/user-attachments/assets/f2e9338e-956e-4685-b909-a7f8d02d7225)


---

## 9. Start the Fabric Network  
```bash
./network.sh up
```
Starts the network by launching peer, orderer, and CA containers, and generates the required cryptographic materials.

## Screenshot 
![Screenshot 2025-04-13 172259](https://github.com/user-attachments/assets/94373585-61e5-4cf1-912e-324a7814864c)

---

## 10. Create a Channel  
```bash
./network.sh createChannel
```
Creates a default channel (usually named `mychannel`) and joins the peers to it.

## Screenshot 
![Screenshot 2025-04-13 172952](https://github.com/user-attachments/assets/debbfd28-95fa-407c-ac39-0439d20b8bed)
![Screenshot 2025-04-13 173050](https://github.com/user-attachments/assets/371e77a4-b7c4-45c2-b98d-d0fc88c83ac0)


---

## 11. Shut Down the Network  
```bash
./network.sh down
```
Stops all containers and deletes the crypto material and artifacts created during the setup.

## Screenshot 
![Screenshot 2025-04-13 173229](https://github.com/user-attachments/assets/2db9a0b7-3949-4f55-b777-0e457bbc97e0)

---

# Solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

/*
Solidity Smart Contract Tutorial - HelloWorld Example

Development Steps:

1. SETUP ENVIRONMENT:
   - Open https://remix.ethereum.org in browser
   - No installation required

2. CREATE CONTRACT FILE:
   - Click "File Explorer" icon (left sidebar)
   - Click "+" button to create new file
   - Name it "HelloWorld.sol"

3. WRITE CONTRACT CODE:
   - Copy and paste this entire file
   - Or type the contract code below

4. COMPILE:
   - Click "Solidity Compiler" icon (3rd icon)
   - Select compiler version 0.8.0+
   - Click "Compile HelloWorld.sol"

5. DEPLOY:
   - Click "Deploy & Run" icon (4th icon)
   - Select "JavaScript VM" environment
   - Click orange "Deploy" button

6. INTERACT:
   - Under "Deployed Contracts":
     a. Click "greeting" to view current message
     b. Type new message in "updateGreeting" field
     c. Click "transact" to update (owner only)
*/

contract HelloWorld {
    string public greeting;
    address public owner;

    constructor() {
        greeting = "Hello Web3 World!";
        owner = msg.sender;
    }

    function updateGreeting(string memory newGreeting) public {
        require(msg.sender == owner, "Only owner can update greeting");
        greeting = newGreeting;
    }

    /*
    CUSTOMIZATION OPTIONS:
    1. Change initial greeting in constructor
    2. Rename contract (HelloWorld)
    3. Modify function names (updateGreeting)
    4. Add new functions as needed
    
    SECURITY OPTIONS:
    1. Implement time-locks for changes
    2. Add multi-signature requirements
    3. Create upgradeability pattern
    
    NEXT STEPS:
    1. Add event emissions for tracking
    2. Write unit tests in JavaScript
    3. Deploy to Ethereum testnet
    */
}
# Blockchain-Practicals
## Question 1
Create a voting system with multiple candidates. Each address can vote only once.
## Code
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract VotingSystem {
    struct Candidate {
        string name;
        uint voteCount;
    }

    mapping(address => bool) public hasVoted;
    Candidate[] public candidates;

    constructor(string[] memory candidateNames) {
        for (uint i = 0; i < candidateNames.length; i++) {
            candidates.push(Candidate(candidateNames[i], 0));
        }
    }

    function vote(uint candidateIndex) public {
        require(!hasVoted[msg.sender], "Already voted");
        require(candidateIndex < candidates.length, "Invalid candidate");

        hasVoted[msg.sender] = true;
        candidates[candidateIndex].voteCount++;
    }

    function getCandidate(uint index) public view returns (string memory, uint) {
        require(index < candidates.length, "Invalid candidate");
        Candidate storage candidate = candidates[index];
        return (candidate.name, candidate.voteCount);
    }

    function getTotalCandidates() public view returns (uint) {
        return candidates.length;
    }
}
```
## Deployment
![Screenshot 2025-05-19 135728](https://github.com/user-attachments/assets/d61eefd1-91c7-42ca-b3c7-dfe171e19c1e)
## Interaction with contract
![Screenshot 2025-05-19 142322](https://github.com/user-attachments/assets/5c1eb904-baa3-4e52-9f85-6d48ae0c53e6)


## Question 2
Write a contract that manages a list of student records (name, roll number). Allow adding and retrieving student data.
## Code
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract StudentRecords {
    struct Student {
        string name;
        uint rollNumber;
    }

    Student[] public students;

    function addStudent(string memory name, uint rollNumber) public {
        students.push(Student(name, rollNumber));
    }

    function getStudent(uint index) public view returns (string memory, uint) {
        require(index < students.length, "Invalid index");
        Student storage student = students[index];
        return (student.name, student.rollNumber);
    }

    function getTotalStudents() public view returns (uint) {
        return students.length;
    }
}
```
## Deployment and Interaction with contract
![Screenshot 2025-05-19 142753](https://github.com/user-attachments/assets/dc25f532-6d26-43ea-8238-9c3e996ed7ad)
## Question 3
Develop a contract that only allows the deployer (owner) to call a specific function (use modifiers).
## Code
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract OwnerOnly {
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    modifier onlyOwner() {
        require(msg.sender == owner, "Not the owner");
        _;
    }

    function ownerFunction() public onlyOwner {
        // Function logic for owner only
    }
}
```
## Deployment and interaction with the contract
![Screenshot 2025-05-19 143610](https://github.com/user-attachments/assets/e7075e24-31d8-49c1-8cf9-2ca06b3a3839)

## Question 4
Write a contract where people can donate Ether and the top 3 donors are tracked
## code
```

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract TopDonors {
    struct Donor {
        address addr;
        uint amount;
    }

    Donor[3] public topDonors;

    function donate() public payable {
        require(msg.value > 0, "Must send some Ether");
        for (uint i = 0; i < 3; i++) {
            if (msg.value > topDonors[i].amount) {
                for (uint j = 2; j > i; j--) {
                    topDonors[j] = topDonors[j - 1];
                }
                topDonors[i] = Donor(msg.sender, msg.value);
                break;
            }
        }
    }

    function getTopDonors() public view returns (Donor[3] memory) {
        return topDonors;
    }
}
```
![Screenshot 2025-05-19 185602](https://github.com/user-attachments/assets/705474b5-7e3e-4082-ac32-a432c0c32eb9)


<br>

## Question 5
Implement a simple auction system where users can place bids, and the highest bidder wins.
## Code
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Auction {
    address public highestBidder;
    uint public highestBid;

    function bid() public payable {
        require(msg.value > highestBid, "Bid too low");

        if (highestBid != 0) {
            payable(highestBidder).transfer(highestBid); // Refund previous
        }

        highestBidder = msg.sender;
        highestBid = msg.value;
    }
}
```
![Screenshot 2025-05-19 190154](https://github.com/user-attachments/assets/b57a6aec-3a06-4db1-b6e9-506391195961)


<br>

## Question 6
Create a contract that splits incoming Ether between 3 fixed addresses.
## Code
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Splitter {
    address payable public addr1;
    address payable public addr2;
    address payable public addr3;

    constructor(address payable _a1, address payable _a2, address payable _a3) {
        addr1 = _a1;
        addr2 = _a2;
        addr3 = _a3;
    }

    receive() external payable {
        uint256 share = msg.value / 3;
        addr1.transfer(share);
        addr2.transfer(share);
        addr3.transfer(msg.value - 2 * share); // Handle remainder
    }
}
```
![Screenshot 2025-05-19 190426](https://github.com/user-attachments/assets/3fcab5c9-83aa-4a70-8b3a-d173de82efbd)


