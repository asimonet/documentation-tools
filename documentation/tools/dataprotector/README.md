# 🔐 DataProtector

DataProtector offers developers methods to create apps that give users unparalleled ownership and privacy over their data.&#x20;

Through DataProtector, users may allow apps to use their data–without ever revealing the data itself. This revolutionary approach to data management relies on:

* end-to-end encryption backed by a confidential computing technology that prevents apps from accessing users’ unencrypted data
* smart contracts that manage apps’ rights to use users’ encrypted data

DataProtector bundles 6 methods:

* **protectData**—that safeguards any data. It takes responsibility for encrypting the data and recording ownership on a smart contract
* **grantAccess**—that authorizes an app to use users’ data without ever revealing the data itself
* **revokeAllAccessObservable**—that revokes all apps' access to users’ data
* **revokeOneAccess**—that revokes an app's access to users’ data
* **fetchProtectedData**—that retrieves data protected by DataProtector
* **fetchGrantedAccess**—that provides the list of authorization with associated apps and users to use existing protected data
