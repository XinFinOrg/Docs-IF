##**1. Website Set-Up**

Note: You will need to have Node 6.X.X version on your local development machine. You can use nvm to easily switch Node versions between different projects.

# **I.Clone the Repository**

To clone the repository, 

- git clone (URL of repository)
- download the repository and extract it.

After cloning the repository, you need to add a file on the repository.


- File location: (root of infactor repository)/Config/config.js 

- 
File content should be copied from default Config.js and paste in config.js

# **II. Install dependencies**

a. Install Node modules

     
      npm install

 

b. Install Angular Modules

      
      bower install

# **III. Deploy Contract**

To connect with XinFin Blockchain, follow these instructions

a. Compile Contract

      
    truffle compile

 

b. Deploy Contract

      
    truffle migrate

# **IV. Start Server**

     npm start

