
## Instructions To Create Pcckage

1. install node.js on pc: https://nodejs.org/en/
2. run this on power shell/vsc terminal: "npm install -g yo generator-code"
* if there is an ERROR: "running scripts is disabled on this system"
* run this on shell as admnin: "Set-ExecutionPolicy RemoteSigned -Scope CurrentUser"
3. type: yo code
4. select: "New Extension Pack" and fill the fields
5. Get a Personal Access Token: create your own organization- https://docs.microsoft.com/azure/devops/organizations/accounts/create-organization
6. screen shot: https://code.visualstudio.com/assets/api/working-with-extensions/publishing-extension/token1.png
7. On the Personal Access Tokens page, select New Token to create a new Personal Access Token and set the following details:
    - Give it a Name
    - Set Organization to All accessible organizations
    - Optionally extend its expiration date
    - Set Scopes to Custom defined and choose the Marketplace > Manage scope
    - screen shot: https://code.visualstudio.com/assets/api/working-with-extensions/publishing-extension/token2.png
8. Select Create and you'll be presented with your newly created Personal Access Token. Copy it, you'll need it to create a publisher.
10. run on terminal: vsce login <publisher name>
11. enter your token
12. go to package.json file
13. in: "extensionPack" paste the names of "extension" that you want to be in your pack for exm: 
    "esbenp.prettier-vscode", (for prettier extension)
    * you can find all the packages names on the market site: https://marketplace.visualstudio.com/vscode
    * click on the extension you want, 
    * look for "more info"
    * on Unique Identifier copy the pack name and paste on your file.
12. for save pack type: "vsce package"
13. for publish pack type: "vsce publish"
    
- how to run old package

1. repet steps 1 and 2
2. in terminal: npm install -g vsce
3. create new token (if old one expaire) get into https://dev.azure.com login to your account and create new token
4. in terminal: vsce login (publisher name)
5. past to new token number.
6. done!
    
   # All Done! You have New Package In VSC Store For Download
