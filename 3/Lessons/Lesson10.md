# 🖥️ How to Install Shopify CLI v3 on Windows

In this guide, we walk through the complete process of installing **Shopify CLI version 3** on a **Windows** system. This updated process simplifies the installation compared to previous versions by removing the need for tools like Chocolatey.

---

## ✅ **System Requirements**

Before installing **Shopify CLI**, ensure the following dependencies are installed:

### **1. Node.js (v14.17 or higher)**

* Visit: [https://nodejs.org/](https://nodejs.org/)
* Download the **LTS (Long Term Support)** version for Windows.
* During installation:

  * Accept default options.
  * Enable the option to install necessary **C++ build tools**.

### **2. Ruby + DevKit (Version 3.1.2-1 or later)**

* Visit: [RubyInstaller](https://rubyinstaller.org/downloads/)
* Download **Ruby+DevKit** (not the version without DevKit).
* During setup:

  * Check the **MSYS2 development toolchain**.
  * After install, keep the option to run `ridk install`.
  * In the terminal that appears, press **Enter** to proceed with defaults (options 1 and 3).
* Verify with:

  ```bash
  ruby -v
  gem list
  ```

### **3. Git**

* Visit: [Git for Windows](https://git-scm.com/)
* Download and install using the default options.
* Verify installation:

  ```bash
  git --version
  ```

### **4. Bundler (Ruby Gem)**

Bundler should be included automatically with the Ruby+DevKit install. Verify with:

```bash
gem list | findstr bundler
```

---

## 📦 **Installing Shopify CLI v3**

Once all prerequisites are installed, proceed with the CLI installation using **npm**:

### **Install via npm (no Chocolatey needed):**

```bash
npm install -g @shopify/cli @shopify/theme
```

* `-g` flag installs the packages globally, making `shopify` command accessible anywhere in the terminal.

### **Verify Installation**

```bash
shopify version
```

You should see a version like `3.23.0`.

---

## ⚠️ Notes & Tips

* **Restart Terminal** after installing each component (Node.js, Ruby, Git) to apply environment variable changes.
* **No need for 7-Zip** unless you are packaging your theme into a `.zip` file later.
* If you had a previous Shopify CLI installation, uninstall it first:

  ```bash
  npm uninstall -g @shopify/cli @shopify/theme
  ```

---

## 🎉 Summary

You’ve successfully installed **Shopify CLI v3** on your Windows machine! You're now ready to start developing themes, deploying apps, and more with the latest tools from Shopify.

In the next lesson, installation on **macOS** will be covered.
