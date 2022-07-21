### RPA CHALLENGE PROJECT ###

[RPA CHALLENGE LINK](https://www.rpachallenge.com/)

### REFrameWork Template ###
**Robotic Enterprise Framework**

### How It Works ###

1. **INITIALIZE PROCESS**
 + ./Framework/*InitiAllSettings* - Load configuration data from Config.xlsx file and from assets
 + ./Framework/*Dispatcher* - Open chrome in the rpachallenge link, download the excel with client data and feed the orchestrator queue called RPAChallenge
 + ./Framework/*InitiAllApplications* - Open Chrome with rpachallenge link on private mode and click in start

2. **GET TRANSACTION DATA**
 + ./Framework/*GetTransactionData* - Fetches transactions from an Orchestrator queue defined by Config("OrchestratorQueueName") or any other configured data source

3. **PROCESS TRANSACTION**
 + *Process* - In the page rpachallenge fills the fields correctly according to the queue data, with dynamic selectors using anchors in the name labels
 + ./Framework/*SetTransactionStatus* - Updates the status of the processed transaction (Orchestrator transactions by default): Success, Business Rule Exception or System Exception

4. **END PROCESS**
 + ./Framework/*CloseAllApplications* - Logs out and closes applications used throughout the process


### To use this project ###

1. Add the path "Teste desenvolvedor RPA" in your orchestrator
2. With the folder created, add the queue "RPAChallenge"
3. In the same folder, create an asset named "Nome_Arquivo" such with the value "\challenge.xlsx"
4. Now you can run the project, have fun!
