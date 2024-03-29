# Create a multicloud IBM Blockchain network 

<br>
<p align="center">
  <img src="docs/doc-gifs/demo.gif">
</p>
<br>


One of the aspects that makes blockchain technology so attractive to developers is the
decentralized nature of the technology - blockchain enables us to bypass middlemen and transact directly
with the network participants in a peer-to-peer manner. Bypassing middlemen enables us to not only 
to increase performance of our operations, but also can decrease cost as well.

The decentralized nature of the technology adds another benefit to our operations, and that is 
high-availability and fault-tolerance. Since the ledger is replicated across all nodes in the 
network, the more decentralized the nodes are (be that they are hosted in different continents, different 
data centers, different clouds, etc.) the more fault tolerant and highly available your operations are.  

Now you may be thinking, "okay, that sounds great, but how do I design my network to be as 
decentralized as possible?". This is where multicloud comes in. 


### Getting started with IBM Blockchain Platform for Multicloud

<b>Disclaimer: to fully run this pattern, (unless you work at IBM) you will have to likely
pay for the IBM Blockchain Platform for multicloud helm chart.</b> 

Furthermore, you will have to pay for some sort of hardware to install 
your ICP network on top of. I am buying my virtual private server 
from IBM Public cloud, but you could easily do so from Azure, Google, AWS,
or just bring your own hardware. Just note that this pattern is only 
tested for the specific IBM Cloud hardware that I am purchasing, so if 
you get errors due to different hardware, it will be difficult to trouble
shoot. Note that the longer your network is running, the more you will
likely have to pay - if you just want to learn the process of configuring 
a multicloud blockchain network, I recommend working through this pattern
and then deleting your network, and turning off your hardware if you 
don't need it to make sure you will not get charged extra for the 
resources you are consuming.

<b>Note: If you are looking for a completely free pattern to get started with, 
you can go [here](https://github.com/IBM/evote) - this pattern will 
enable you to try the IBM Blockchain Platform for free, only on IBM Cloud,
for 30-days.</b> 
 
 All you have to do is put in your credit card and then upgrade your cloud account to <b>Pay as You Go</b>, select the free
Kubernetes service, and then deploy the IBM Blockchain Platform on that 
free Kubernetes cluster, and you will be ready to go. There will be no
charges on your credit card as long as you use the free cluster.

### Overview





 If 
you are an IBMer, then you should be able to run this for free, but other than that, you will have to 
purchase the IBM Blockchain Platform 

The IBM Blockchain Platform - which leverages the open-source Hyperledger Fabric project to rapidly build 
and scale blockchain networks - can be deployed accross public and private clouds, your own data center, 
and third-party public clouds (such as AWS). The deployment is available through <b>IBM Cloud Private</b>
IBM's Kubernetes based platform for container orchestration. This means that you can either take your own 
server, a virtual server running on AWS, or a virtual server running on IBM Cloud (what we will show you 
now), install IBM Cloud Private on the server, and then start running the IBM Blockchain Platform on the 
hardware of your choice, in the location of your choice! Hopefully this gets you somewhat excited, so let's 
get started! 

### Getting your hardware

First thing's first. We need a server to run our Kubernetes platform on top of..so let's go ahead and 
make use of IBM's public cloud. 


After that, we use our drivers license number to submit our vote, during which the application checks 
if this drivers license number has voted before and tells the user they have already submitted a vote 
if so. If all goes well, the political party which the voter has chosen is given a vote, and the world
state is updated. The application then updates our current standings of the election to show how many 
votes each political party currently has. 

Since each transaction that is submitted to the ordering service must have a signature from a valid
public-private key pair, we can trace back each transaction to a registered voter of the application, 
in the case of an audit.

In conclusion, although this is a simple application, the developer can see how they can implement a 
Hyperledger Fabric web-app to decrease the chance of election-meddling, and enhance a voting application
by using blockchain technology. 

When the reader has completed this code pattern, they will understand how to:

* Create, build, and use the IBM Blockchain Platform service.
* Build a blockchain back-end using Hyperledger Fabric API's
* Create and use a (free) Kubernetes Cluster to deploy and monitor our 
Hyperledger Fabric nodes.
* Deploy a Node.js app that will interact with our deployed smart contract.

# Flow Diagram
<br>
<p align="center">
  <img src="docs/app-architecture.png">
</p>
<br>

# Flow Description
1. The blockchain operator sets up the IBM Blockchain Platform 2.0 service.


# Included components
*	[IBM Blockchain Platform](https://console.bluemix.net/docs/services/blockchain/howto/ibp-v2-deploy-iks.html#ibp-v2-deploy-iks) gives you total control of your blockchain network with a user interface that can simplify and accelerate your journey to deploy and manage blockchain components on the IBM Cloud Kubernetes Service.
*	[IBM Cloud Private](https://www.ibm.com/cloud/container-service) creates a cluster of compute hosts and deploys highly available containers. A Kubernetes cluster lets you securely manage the resources that you need to quickly deploy, update, and scale applications.

## Featured technologies
+ [Hyperledger Fabric v1.4](https://hyperledger-fabric.readthedocs.io) is a platform for distributed ledger solutions, underpinned by a modular architecture that delivers high degrees of confidentiality, resiliency, flexibility, and scalability.
+ [Node.js](https://nodejs.org) is an open source, cross-platform JavaScript run-time environment that executes server-side JavaScript code.
+ [Vue.js 2.6.10](https://vuejs.org/) Vue.js is an open-source JavaScript framework for building user interfaces and single-page applications.

# Watch the Video - Intro (Cloud)

[![](docs/ibpVideo.png)](https://www.youtube.com/watch?v=ny8iif6ZXRU)

# Watch the Video - Build and Run the App (Cloud)

[![](docs/ibpVideo2.png)](https://www.youtube.com/watch?v=mkVUW1KroTI)

# Watch the Video - Code walkthrough (User Authentication)

[![](docs/userAuth.png)](https://www.youtube.com/watch?v=8uJSHW3Rpzs)

# Watch the Video - Code walkthrough (Routes)

[![](docs/routes.png)](https://www.youtube.com/watch?v=iajsJiIC7oU)

**🚧🚧Note: you will need Node 8.x to run this pattern!🚧🚧**

For example, to install and run Node 8.9.0: 

```bash
  brew install nvm
  nvm install 8.9.0
  nvm use 8.9.0
```  


## Prerequisites (Cloud)

This Cloud pattern assumes you have an **IBM Cloud account**.
  - [IBM Cloud account](https://tinyurl.com/y4mzxow5)
  - [Node v8.x or greater and npm v5.x or greater](https://nodejs.org/en/download/)

You do not technically need VSCode or the IBM Blockchain Platform extension for VSCode if you are running the 
Cloud pattern, but if you want to make any changes to the smart contract, you will need the
extension to package your smart contract project. 


## Prerequisites (Local)
If you want to run this pattern locally, without any Cloud services, then all you need is VSCode and the
IBM Blockchain Platform extension. 
- [Install VSCode](https://code.visualstudio.com/download)
- [Install IBM Blockchain Platform Extension for VSCode](https://github.com/IBM-Blockchain/blockchain-vscode-extension)
- [Node v8.x or greater and npm v5.x or greater](https://nodejs.org/en/download/)

# Steps (Local Deployment)
> To run a local network, you can find steps [here](./docs/run-local.md).

# Steps (Cloud Deployment)
1. [Clone the Repo](#step-1-clone-the-repo)
2. [Create IBM Cloud services](#step-2-create-ibm-cloud-services)
3. [Build a network](#step-3-build-a-network)
4. [Deploy voterContract Smart Contract on the network](#step-4-deploy-voterContract-smart-contract-on-the-network)
5. [Connect application to the network](#step-5-connect-application-to-the-network)
6. [Run the application](#step-6-run-the-application)

## Step 1. Clone the Repo

Git clone this repo onto your computer in the destination of your choice, then go into the web-app folder:
```
HoreaPorutiu$ git clone https://github.com/IBM/evote
```

## Step 2. Create IBM Cloud services

* Create the [IBM Cloud Kubernetes Service](https://cloud.ibm.com/catalog/infrastructure/containers-kubernetes).  You can find the service in the `Catalog`.  For this code pattern, we can use the `Free` cluster, and give it a name.  Note, that the IBM Cloud allows one instance of a free cluster and expires after 30 days. <b>The cluster takes around 10-15
minutes to provision, so please be patient!</b>

<br>
<p align="center">
  <img src="docs/doc-gifs/createIKS.gif">
</p>
<br>

* Create the [IBM Blockchain Platform](https://console.bluemix.net/catalog/services/blockchain/) service on the IBM Cloud.  You can find the service in the `Catalog`, and give a name.

* After your Kubernetes cluster is up and running, you can deploy your IBM Blockchain Platform service on the cluster. The service walks through few steps and finds your cluster on the IBM Cloud to deploy the service on.

* In the gif below, you can see me choosing my free cluster to deploy my IBM Blockchain Platform.

* Once the Blockchain Platform is deployed on the Kubernetes cluster (which can 
take a couple of minutes, you can launch the console to start operating on your
blockchain network by clicking on *Launch the IBM Blockchain Platform*.

<br>
<p align="center">
  <img src="docs/doc-gifs/createIBP.gif">
</p>
<br>


## Step 3. Build a network

We will build a network as provided by the IBM Blockchain Platform [documentation](https://console.bluemix.net/docs/services/blockchain/howto/ibp-console-build-network.html#ibp-console-build-network).  This will include creating a channel with a single peer organization with its own MSP and CA (Certificate Authority), and an orderer organization with its own MSP and CA. We will create the respective identities to deploy peers and operate nodes.

### Create your organization and your entry point to your blockchain

* #### Create your Voter Organization CA
  - Click <b>Add Certificate Authority</b>.
  - Click <b>IBM Cloud</b> under <b>Create Certificate Authority</b> and <b>Next</b>.
  - Give it a <b>Display name</b> of `Voter CA`. Note that the gif names the 
  certificate a more generic name.  
  - Specify an <b>Admin ID</b> of `admin` and <b>Admin Secret</b> of `adminpw`.

<br>
<p align="center">
  <img src="docs/doc-gifs/voterCA.gif">
</p>
<br>


* #### Use your CA to register identities
  - Select the <b>Voter CA</b> Certificate Authority that we created.
  - First, we will register an admin for our voter organization. Click on the <b>Register User</b> button.  Give an <b>Enroll ID</b> of `voterAdmin`, and <b>Enroll Secret</b> of `voterAdminpw`. Set the <b>Type</b> for this identity as `client`. We will leave the <b>Maximum enrollments</b> and <b>Add Attributes</b> fields blank. Click <b>Next</b>. Then on the next page,
  click <b>Register User</b>.
  - We will repeat the process to create an identity of the peer. Click on the <b>Register User</b> button.  Give an <b>Enroll ID</b> of `peer1`, and <b>Enroll Secret</b> of `peer1pw`. Set the <b>Type</b> for this identity as `peer`. We will leave the <b>Maximum enrollments</b> and <b>Add Attributes</b> fields blank. Click <b>Next</b>. Then on the next page,
  click <b>Register User</b>.

<br>
<p align="center">
  <img src="docs/doc-gifs/registerIdentities.gif">
</p>
<br>


* #### Create the peer organization MSP definition
  - Navigate to the <b>Organizations</b> tab in the left navigation and click <b>Create MSP definition</b>.
  - Enter the <b>MSP Display name</b> as `Voter MSP` and an <b>MSP ID</b> of `votermsp`.
  - Under <b>Root Certificate Authority</b> details, specify the peer CA that we created `Voter CA` as the root CA for the organization.
  - Give the <b>Enroll ID</b> and <b>Enroll secret</b> for your organization admin, `voterAdmin` and `voterAdminpw`. Then, give the Identity name, `Voter Admin`.
  - Click the <b>Generate</b> button to enroll this identity as the admin of your organization and export the identity to the wallet. Click <b>Export</b> to export the admin certificates to your file system. Finally click <b>Create MSP definition</b>.

<br>
<p align="center">
  <img src="docs/doc-gifs/voterMSP.gif">
</p>
<br>


* Create a peer
  - On the <b>Nodes</b> page, click <b>Add peer</b>.
  - Click <b>IBM Cloud</b> under Create a new peer and <b>Next</b>.
  - Give your peer a <b>Display name</b> of `Voter Peer`.
  - On the next screen, select `Voter CA` as your <b>Certificate Authority</b>. Then, give the <b>Enroll ID</b> and <b>Enroll secret</b> for the peer identity that you created for your peer, `peer1`, and `peer1pw`. Then, select the <b>Administrator Certificate (from MSP)</b>, `Voter MSP`, from the drop-down list and click <b>Next</b>.
  - Give the <b>TLS Enroll ID</b>, `admin`, and <b>TLS Enroll secret</b>, `adminpw`, the same values are the Enroll ID and Enroll secret that you gave when creating the CA.  Leave the <b>TLS CSR hostname</b> blank.
  - The last side panel will ask you to <b>Associate an identity</b> and make it the admin of your peer. Select your peer admin identity `Voter Admin`.
  - Review the summary and click <b>Submit</b>.

<br>
<p align="center">
  <img src="docs/doc-gifs/voterPeer.gif">
</p>
<br>

### Create the node that orders transactions

* #### Create your orderer organization CA
  - Click <b>Add Certificate Authority</b>.
  - Click <b>IBM Cloud</b> under <b>Create Certificate Authority</b> and <b>Next</b>.
  - Give it a unique <b>Display name</b> of `Orderer CA`.  
  - Specify an <b>Admin ID</b> of `admin` and <b>Admin Secret</b> of `adminpw`.

<br>
<p align="center">
  <img src="docs/doc-gifs/ordererCA.gif">
</p>
<br>

* #### Use your CA to register orderer and orderer admin identities
  - In the <b>Nodes</b> tab, select the <b>Orderer CA</b> Certificate Authority that we created.
  - First, we will register an admin for our organization. Click on the <b>Register User</b> button.  Give an <b>Enroll ID</b> of `ordererAdmin`, and <b>Enroll Secret</b> of `ordererAdminpw`. Set the <b>Type</b> for this identity as `client`. We will leave the <b>Maximum enrollments</b> and <b>Add Attributes</b> fields blank. Click <b>Next</b>. Then on the next page,
  click <b>Register User</b>.
  - We will repeat the process to create an identity of the orderer. Click on the <b>Register User</b> button.  Give an <b>Enroll ID</b> of `orderer1`, and <b>Enroll Secret</b> of `orderer1pw`.  Click <b>Next</b>.  Set the <b>Type</b> for this identity as `peer`. We will leave the <b>Maximum enrollments</b> and <b>Add Attributes</b> fields blank. Click <b>Next</b>. Then on the next page,
  click <b>Register User</b>.

<br>
<p align="center">
  <img src="docs/doc-gifs/ordererIdentities.gif">
</p>
<br>


* #### Create the orderer organization MSP definition
  - Navigate to the <b>Organizations</b> tab in the left navigation and click <b>Create MSP definition</b>.
  - Enter the <b>MSP Display name</b> as `Orderer MSP` and an <b>MSP ID</b> of `orderermsp`.
  - Under <b>Root Certificate Authority</b> details, specify the peer CA that we created `Orderer CA` as the root CA for the organization.
  - Give the <b>Enroll ID</b> and <b>Enroll secret</b> for your organization admin, `ordererAdmin` and `ordererAdminpw`. Then, give the <b>Identity name</b>, `Orderer Admin`.
  - Click the <b>Generate</b> button to enroll this identity as the admin of your organization and export the identity to the wallet. Click <b>Export</b> to export the admin certificates to your file system. Finally click <b>Create MSP definition</b>.

<br>
<p align="center">
  <img src="docs/doc-gifs/ordererMSP.gif">
</p>
<br>

* #### Create an orderer
  - On the <b>Nodes</b> page, click <b>Add orderer</b>.
  - Click <b>IBM Cloud</b> and proceed with <b>Next</b>.
  - Give your peer a <b>Display name</b> of `Orderer`.
  - On the next screen, select `Orderer CA` as your <b>Certificate Authority</b>. Then, give the <b>Enroll ID</b> and <b>Enroll secret</b> for the peer identity that you created for your orderer, `orderer1`, and `orderer1pw`. Then, select the <b>Administrator Certificate (from MSP)</b>, `Orderer MSP`, from the drop-down list and click <b>Next</b>.
  - Give the <b>TLS Enroll ID</b>, `admin`, and <b>TLS Enroll secret</b>, `adminpw`, the same values are the Enroll ID and Enroll secret that you gave when creating the CA.  Leave the <b>TLS CSR hostname</b> blank.
  - The last side panel will ask to <b>Associate an identity</b> and make it the admin of your peer. Select your peer admin identity `Orderer Admin`.
  - Review the summary and click <b>Submit</b>.

<br>
<p align="center">
  <img src="docs/doc-gifs/createOrderer.gif">
</p>
<br>

* #### Add organization as Consortium Member on the orderer to transact
  - Navigate to the <b>Nodes</b> tab, and click on the <b>Orderer</b> that we created.
  - Under <b>Consortium Members</b>, click <b>Add organization</b>.
  - From the drop-down list, select `Voter MSP`, as this is the MSP that represents the peer's Voter organization.
  - Click <b>Submit</b>.

<br>
<p align="center">
  <img src="docs/doc-gifs/consortium.gif">
</p>
<br>


### Create and join channel

* #### Create the channel
  - Navigate to the <b>Channels</b> tab in the left navigation.
  - Click <b>Create channel</b>.
  - Give the channel a name, `mychannel`.
  - Select the orderer you created, `Orderer` from the orderers drop-down list.
  - Under <b>Organizations</b>, select *Voter MSP* and then click *Add*. Next make your organization an <b>Operator</b>.
  - For the channel creator organization, select the MSP identifying the organization from the drop-down list. This should be `Voter MSP (votermsp)`.
  - Associate available identity as `Voter Admin`.
  - Click <b>Create</b>.

<br>
<p align="center">
  <img src="docs/doc-gifs/createChannel.gif">
</p>
<br>


* #### Join your peer to the channel
  - Click <b>Join channel</b> to launch the side panels.
  - Select your `Orderer` and click <b>Next</b>.
  - Enter the name of the channel you just created. `mychannel` and click <b>Next</b>.
  - Select which peers you want to join the channel, click `Voter Peer` .
  - Click <b>Submit</b>.

<br>
<p align="center">
  <img src="docs/doc-gifs/joinChannel.gif">
</p>
<br>

## Step 4. Deploy voterContract Smart Contract on the network

* #### Install a smart contract
  - Click the <b>Smart contracts</b> tab to install the smart contract.
  - Click <b>Install smart contract</b> to upload the voterContract smart contract package file, which is in the root of the repo we cloned - the file
  is called `voterContract.cds`.
  - Click on <b>Add file</b> and find your packaged smart contract.  
  - Once the contract is uploaded, click <b>Install</b>.


<br>
<p align="center">
  <img src="docs/doc-gifs/installContract.gif">
</p>
<br>

* #### Instantiate smart contract
  - On the smart contracts tab, find the smart contract from the list installed on your peers and click <b>Instantiate</b> from the overflow menu on the right side of the row.
  - On the side panel that opens, select the channel, `mychannel` to instantiate the smart contract on. Click <b>Next</b>.
  - Select the organization members to be included in the policy, `votermsp`.  Click <b>Next</b>.
  - Give <b>Function name</b> of `init` and leave <b>Arguments</b> blank.
  - Click <b>Instantiate</b>.

<br>
<p align="center">
  <img src="docs/doc-gifs/instantiateContract.gif">
</p>
<br>

## Step 5. Connect application to the network

* #### Connect with sdk through connection profile
  - Under the Instantiated Smart Contract, click on `Connect with SDK` from the overflow menu on the right side of the row.
  - Choose from the dropdown for <b>MSP for connection</b>, `votermsp`.
  - Choose from <b>Certificate Authority</b> dropdown, `Voter CA`.
  - Download the connection profile by scrolling down and clicking <b>Download Connection Profile</b>.  This will download the connection json which we will use soon to establish connection.
  - You can click <b>Close</b> once the download completes.

<br>
<p align="center">
  <img src="docs/doc-gifs/downloadCCP.gif">
</p>
<br>

* #### Create an application admin
  - Go to the <b>Nodes</b> tab on the left bar, and under <b>Certificate Authorities</b>, choose your organization CA, <b>Voter CA</b>.
  - Click on <b>Register user</b>.
  - Give an <b>Enroll ID</b> and <b>Enroll Secret</b> to administer your application users, `app-admin` and `app-adminpw`.
  - Choose `client` as <b>Type</b>.
  - You can leave the <b>Maximum enrollments</b> blank.
  - Under <b>Attributes</b>, click on <b>Add attribute</b>.  Give attribute as `hf.Registrar.Roles` = `*`.  This will allow this identity to act as registrar and issues identities for our app.  Click <b>Add-attribute</b>.
  - Click <b>Register</b>.

<br>
<p align="center">
  <img src="docs/doc-gifs/appAdmin.gif">
</p>
<br>


* #### Update application connection
  - Copy the connection profile you downloaded into [server folder](server)
  - Rename the connection profile you downloaded **ibpConnection.json**
  - Update the [config.json](server/config.json) file with:
    - `ibpConnection.json`.
    - The <b>enroll id</b> and <b>enroll secret</b> for your app admin, which we earlier provided as `app-admin` and `app-adminpw`.
    - The orgMSP ID, which we provided as `votermsp`.
    - The caName, which can be found in your connection json file under "organization" -> "org1msp" -> certificateAuthorities". This would be like an IP address and a port. This is circled in red above.
    - The username you would like to register.
    - Update gateway discovery to `{ enabled: true, asLocalhost: false }` to connect to IBP.

<br>
<p align="center">
  <img src="docs/doc-gifs/updateConfig.gif">
</p>
<br>

- Once you are done, the final version of the **config.json** should look something like this:

```js
{
    "connection_file": "ibpConnection.json",
    "appAdmin": "app-admin",
    "appAdminSecret": "app-adminpw",
    "orgMSPID": "votermsp",
    "caName": "173.193.106.28:32634",
    "userName": "V1",
    "gatewayDiscovery": { "enabled": true, "asLocalhost": false }
}
```


## Step 6. Run the application

* #### Enroll admin
  - First, navigate to the `web-app/server` directory, and install the node dependencies.
    ```bash
    cd web-app/server
    npm install
    ```
  
  - Run the `enrollAdmin.js` script
    ```bash
    node enrollAdmin.js
    ```

  - You should see the following in the terminal:
    ```bash
    msg: Successfully enrolled admin user app-admin and imported it into the wallet
    ```

  - Start the server:
    ```bash
    npm start
    ```

<br>
<p align="center">
  <img src="docs/doc-gifs/startServer.gif">
</p>
<br>

* #### Start the web client
  - In a new terminal, open the `web-app/client` folder from the root directory. 
  Install the required dependencies with `npm install`.
    ```bash
    cd web-app/client
    npm install
    ```

  - Start the client:
    ```bash
    npm run serve
    ```

  - In a browser of your choice, go to http://localhost:8080/#/.  If all goes well, you should see 
  something like the gif below:

<br>
<p align="center">
  <img src="docs/doc-gifs/runClient.gif">
</p>
<br>

You can find the app running at http://localhost:8080/  If all goes well, you should be greeted 
with the homepage that says <b>2020 Presidential Election</b>

Now, we can start interacting with the app.

First, we need to register as a voter, and create our digital identity with 
which we will submit our vote with. To do this, we will need to enter 
a uniqueId (drivers license) with a registrarId, and our first and last names.
After we do that, and click `register` the world state will be updated with 
our voterId and our name and registrarId.

If all goes well, you should see `voter with voterId {} is updated in the world state. Use voterId to login above.`
<b>Note: on the first try, the app can take a second to start up. If you click on `register` and nothing 
happens, try to fill in the form and click register again!</b>

Next, we can login to the app with our voterId.

Once we login, we can cast our vote. We will use our voterId again to cast our 
vote. Since we are voting for the presidential
election for 2020, we can choose the party of our liking. Once we are done, we
can choose submit, and then our vote is cast. As long as this voterId hasn't 
voted before, all is well. Next, we can view the poll standings by clicking
`Get Poll Standings` and clicking `Check Poll`. This will query the world 
state and get the current number of votes for each political party.

<br>
<p align="center">
  <img src="docs/doc-gifs/demo.gif">
</p>
<br>

If we want to query for a particular voterId, we can do so in the `Query by Key` tab.
If we want to query by object, we can do so by clicking on the `Query by Type` 
tab, and entering a type, such as `voter`. This will return all voter objects 
that are currently in the state. `QueryAll` will return all objects in the state.

<br>
<p align="center">
  <img src="docs/doc-gifs/query.gif">
</p>
<br>

## Extending the code pattern
Pull requests and contribution are always welcome. Remember that a code pattern is a path to a solution, 
and not a complete solution on its own. To make this a more complete solution,
this application can be expanded in a couple of ways:

  * Use an API to verify the drivers license to make sure it is valid, and registered with the DMV.
  * Use a more complex consensus mechanism where multiple organizations (DMV, US Federal Government, US State
  Government) have to approve a vote before it is successfully recorded onto the blockchain.
  * Use ordering service which uses Raft consensus mechanism.

## Related Links
* [Hyperledger Fabric Docs](http://hyperledger-fabric.readthedocs.io/en/latest/)
* [IBM Code Patterns for Blockchain](https://developer.ibm.com/patterns/category/blockchain/)

## License
This code pattern is licensed under the Apache Software License, Version 2. Separate third-party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1 (DCO)](https://developercertificate.org/) and the [Apache Software License, Version 2](https://www.apache.org/licenses/LICENSE-2.0.txt).

[Apache Software License (ASL) FAQ](https://www.apache.org/foundation/license-faq.html#WhatDoesItMEAN)

