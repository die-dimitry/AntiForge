# AntiForge
AntiForge is a DApp Supply chain system which uses blockchain technology to validate product authenticity and prevent forgery.

Steps To install:

Pre-required Setups
XAMPP, Ganache, MetaMask and Truffle(Truffle can be installed using NPM).

Clone the reporsitory;
git clone https://github.com/die-dimitry/AntiForge/

Ganache:
Open Ganache and Create new Workspace.
You'll get multiple wallets, copy the private key which you'll get by Clicking on Key icon on right of wallet.

Setup Metamask:
In a browser installed with metamask plugin, create a new network and use the details from Ganache to fill it:
Name, RPC Server (http://localhost:7545), Client ID (1337) & Symbol.
Then in Metamask under Accounts click on Import Account & Paste the Private Key you copied from Ganache.
Once your wallet is loaded open Remix IDE on your Browser.

Remix IDE
Open a solidity file name 'smartcontract.sol' , paste it in IDE and Compile it. Make sure you're using '0.6.12 + commit.27d51765' comipler.
If you see any Errors in compilation ask ChatGPT.
To Deploy the code Click on 'Deploy & run Transactions' -> Choose Environment as 'Inject Provider - Metamask'.
Now, you'll get Metmask pop up where you'll have to choose account which has credits and cross verify in RemixIDE too if same wallet account was added.
Then click on Deploy and Click on Cofirm on Metmask Popup window.

Copy the Contract Address which you can get under 'Deployed Contract' by clicking on copy Symbol and paste it in app.js. You'll see a comment box for where to paste
contract address.
Copy the Contract ABI from 'Solidity Compiler' tab. You should see tiny 'ABI' at the bottom below Compilation Details. Paste ABI in app.js file.
Follow comments in app.js file to know where to paste it. Its basically code inside square bracket.

Open XAMPP and run Apache and MySql.
Move Entire Folder at xampp/htdocs/AntiForge if you haven't done it yet. You can find Xampp folder in C drive if using Windows, while its different for other OS.
Before starting the web dashboard, open 'localhost/phpmyadmin' on browser and add a Database with name as 'supplychain' then click on Import and Import the Database file
from '/AntiForge/sql/supplychain.sql'
If you get all things done you should be able to access the dashboard from 'localhost/AntiForge'.


At login page you can use 'suhail@antiforge.com' & 'password' to login and genrate QR Codes for products, similarly you can signup.
Also, passwords in database are MD5 hashed.

ThankYou; Feel free to raise issues if you're having problem else ask chatGPT.
