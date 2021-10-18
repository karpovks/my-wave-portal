# Basic Sample Hardhat Project

This project demonstrates a basic Hardhat use case. It comes with a sample contract, a test for that contract, a sample script that deploys that contract, and an example of a task implementation, which simply lists the available accounts.

Try running some of the following tasks:

```shell
npx hardhat accounts
npx hardhat compile
npx hardhat clean
npx hardhat test
npx hardhat node
node scripts/sample-script.js
npx hardhat help
```

---

✈️ Re-deploy
So, now that we've updated our contract we need to do a few things:

1. We need to deploy it again.

2. We need to update the contract address on our frontend.

3. We need to update the abi file on our frontend. 

People constantly forget to do these 3 steps when they change their contract. Don't forget lol.

Why do we need to do all this? Well, it's because smart contracts are immutable. They can't change. They're permanent. That means changing a contract requires a full redeploy. This will also reset all the variables since it'd be treated as a brand new contract. That means we'd lose all our wave data if we wanted to update the contract's code.

Bonus: In #general-chill-chat, can anyone tell me some solutions here? Where else could we store our wave data where we could update our contract's code and keep our original data around? There are quite a few solutions here let me know what you find!

So what you'll need to do now is:

1. Deploy again using npx hardhat run scripts/deploy.js --network rinkeby

2. Change contractAddress in App.js to be the new contract address we got from the step above in the terminal just like we did before the first time we deployed.

3. Get the updated abi file from artifacts like we did before and copy-paste it into Replit just like we did before. If you forgot how to do this be sure to revisit the lesson here and watch the video I made on ABI files by clicking here.

Again -- you need to do this every time you change your contracts code.

---

Replit Link for React Front End: https://replit.com/@KurtKarpov/waveportal-starter-project-1#src/App.js