# 🛠️ Build your iApp

> Reading time 🕒 10 mins

<div class="hero">
  <div class="hero-content">
    <h2>Time to build!</h2>
    <p>Let's build an iExec App that can process protected data in a secure environment.</p>
  </div>
</div>

<div class="solution-note">
<p>An iExec App (iApp) runs in a Trusted Execution Environment (TEE), it can process data in a secure environment.</p>
</div>

This guide will help you set up, test, deploy and run your iApp using the
[`iapp-cli`](https://github.com/iExecBlockchainComputing/iapp/tree/main/cli)
tool. Follow the instructions carefully for a smooth development experience.

## 📋 Prerequisites

Before getting started, ensure you have the following:

<div class="requirements-list">
  <div class="requirement-item">
    <div class="req-title">📦 Node.js v18+</div>
    <a target="_blank" href="https://nodejs.org/en/">Download →</a>
  </div>

  <div class="requirement-item">
    <div class="req-title">📦 NPM</div>
    <a target="_blank" href="https://www.npmjs.com/get-npm">Download →</a>
  </div>
  
  <div class="requirement-item">
    <div class="req-title">🐳 Docker</div>
    <a target="_blank" href="https://www.docker.com/">Download →</a>
  </div>

  <div class="requirement-item">
    <div class="req-title">🐳 Docker Hub Account</div>
    <a target="_blank" href="https://hub.docker.com/">Sign Up →</a>
  </div>
  
  <div class="requirement-item">
    <div class="req-title">🔑 Private Key</div>
    <a target="_blank" href="https://support.metamask.io/configure/accounts/how-to-export-an-accounts-private-key/">From your Ethereum wallet (e.g., MetaMask)</a>
  </div>
</div>

<div class="solution-note">
  <p>Don't worry! All passwords and private keys used in this tutorial stay on your machine and aren’t shared with anyone. You’ll only need them to run the <code>iApp run</code> command.</p>
</div>

## 💾 Installation (win / mac / linux)

First, you need to install the `iapp-cli` package. Open your terminal and run:

```sh
npm i -g @iexec/iapp-maker
```

You can check if the installation was successful by running:

```sh
iapp --version
```

## 🛠️ Initialize Framework

To initialize the working directory for developing your iApp, use the
`iapp init` command. This command sets up the necessary project structure and
files.

```sh
mkdir iexec-test
cd iexec-test
iapp init
```

You will be prompted with the following message:

```sh
  ___    _    ____  ____
 |_ _|  / \  |  _ \|  _ \
  | |  / _ \ | |_) | |_) |
  | | / ___ \|  __/|  __/
 |___/_/   \_\_|   |_|

✔ What's your project name? (A folder with this name will be created) ...
? What kind of project do you want to init?
  > Hello World - iapp quick start
    Advanced
```

<div class="solution-note">
  <p>We recommend selecting <span class="highlight">"Hello World"</span> to quickly discover how iApp works!</p>
</div>

A new folder was created, it contains a very simple Node.js application, with
the main code being located in `app.js`.

## 🧪 Test Your iApp

To test your iApp, use the `iapp test` command. This command will invoke your
locally installed Node.js and run the `app.js` file.

### 🧩 Using Arguments

You can pass arguments to your iApp using the `--args` option. This allows you
to provide necessary inputs during runtime.

```sh
iapp test --args your-name
```

### Using Protected Data

If your iApp requires protected data, you can use the `--protectedData` option
to specify the data to be used.

```sh
iapp test --protectedData default
```

## 🚀 Deploy Your iApp

Deploy your iApp on the iExec protocol. You need to have your Docker daemon
running to build the Docker image.

<div class="process-steps">
  <div class="step">
    <span class="step-number">1</span>
    <span>Go to <a href="https://hub.docker.com/settings/security" target="_blank">Docker Hub Security Settings</a></span>
  </div>
  <div class="step">
    <span class="step-number">2</span>
    <span>Click "Personal access tokens" → "Generate new token"</span>
  </div>
  <div class="step">
    <span class="step-number">3</span>
    <span>Name it "Test iExec iApp CLI"</span>
  </div>
  <div class="step">
    <span class="step-number">4</span>
    <span>Select "Read & Write" permissions</span>
  </div>
  <div class="step">
    <span class="step-number">5</span>
    <span>Save your token securely</span>
  </div>
</div>

Once you have your token, you can deploy your iApp using the following command:

```sh
iapp deploy
```

<div class="solution-note">
  <p>Make sure to save your <span class="highlight">iApp address</span> after deployment - you'll need it later!</p>
</div>

## 🏃 Run Your iApp

Now you can run your application:

```sh
iapp run <my-iapp-address>
```

## 🎯 Key takeaways

<div class="key-takeaways">
  <div class="takeaway-item">
    <span class="takeaway-icon">🔒</span>
    <div class="takeaway-content">
      <strong>iApps:</strong> Special applications that run in TEEs to process protected data
    </div>
  </div>
  <div class="takeaway-item">
    <span class="takeaway-icon">🛠️</span>
    <div class="takeaway-content">
      <strong>iApp CLI:</strong> Command-line tool for building, testing, and deploying iApps
    </div>
  </div>
  <div class="takeaway-item">
    <span class="takeaway-icon">🔐</span>
    <div class="takeaway-content">
      <strong>Protected Data:</strong> Can be integrated and processed securely in your iApp
    </div>
  </div>
  <div class="takeaway-item">
    <span class="takeaway-icon">⛓️</span>
    <div class="takeaway-content">
      <strong>Deployment:</strong> Apps are deployed on iExec protocol to run in trusted environments
    </div>
  </div>
</div>

<div class="solution-note-green">
  <p>Next up: We'll learn how to authorize our iApp and users to access protected data! 🚀</p>
</div>
