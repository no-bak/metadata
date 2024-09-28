# Nobak DApp Metadata

Welcome to the **Nobak DApp Metadata**! This repository is dedicated to hosting metadata files for Stellar decentralized applications (dApps) that integrate with the Nobak Mobile Expo App. By contributing your dApp's metadata here, you make it easier for users to discover and connect with your application through WalletConnect.

## Table of Contents

- [Nobak DApp Metadata](#nobak-dapp-metadata)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Metadata Structure](#metadata-structure)
    - [Field Definitions](#field-definitions)
  - [How to Contribute](#how-to-contribute)
    - [Adding Your dApp](#adding-your-dapp)
    - [Updating Existing Metadata](#updating-existing-metadata)
    - [Contribution Guidelines](#contribution-guidelines)
  - [License](#license)
  - [Contact](#contact)

## Introduction

The `metadata.json` file serves as a standardized way to provide essential information about your Stellar dApp. This metadata allows wallets like Nobak to display your dApp correctly and enable users to connect via WalletConnect seamlessly.

By following the recommended structure, we ensure consistency and interoperability across the Stellar ecosystem, enhancing the user experience and promoting your dApp effectively.

## Metadata Structure

Below is the recommended structure for the `metadata.json` file:

```json
{
  "name": "Stellar DApp Name",
  "description": "A brief description of the dApp.",
  "category": "Finance",
  "url": "https://stellar-dapp.com",
  "logo": "https://stellar-dapp.com/logo.png",
  "logoBackground": "#FFFFFF",
  "chains": ["Stellar"],
  "permissions": ["read_account", "write_transactions"],
  "social": {
    "twitter": "https://twitter.com/stellar_dapp",
    "discord": "https://discord.gg/stellar_dapp",
    "github": "https://github.com/stellar-dapp"
  },
  "tags": ["DeFi", "Exchange", "Lending"],
  "version": "1.0.0"
}
```

### Field Definitions

- **`name`** *(string, required)*:  
  The display name of your dApp. This should be the official name that users recognize.

- **`description`** *(string, required)*:  
  A brief description of your dApp's functionality and purpose. Keep it concise and informative.

- **`category`** *(string, required)*:  
  The primary category of your dApp, such as "Finance", "Gaming", or "Social". This helps users find your dApp based on their interests.

- **`url`** *(string, required)*:  
  The official website URL of your dApp. This should be a secure (HTTPS) link.

- **`logo`** *(string, required)*:  
  A URL to your dApp's logo image. Preferably a square PNG with transparent background for optimal display.

- **`logoBackground`** *(string, optional)*:  
  A hex color code (e.g., `#FFFFFF`) for the background when displaying your logo. Useful if your logo requires a specific background for visibility.

- **`chains`** *(array of strings, required)*:  
  Supported blockchain networks. For Stellar dApps, include `"Stellar"`.

- **`permissions`** *(array of strings, required)*:  
  Permissions required by your dApp for operation. Examples include `"read_account"`, `"write_transactions"`.

- **`social`** *(object, optional)*:  
  Links to your social media and community channels. This helps users connect with your community.

  - **`twitter`** *(string, optional)*:  
    Your dApp's official Twitter profile URL.

  - **`discord`** *(string, optional)*:  
    Invite URL to your Discord server.

  - **`github`** *(string, optional)*:  
    URL to your GitHub repository or organization.

- **`tags`** *(array of strings, optional)*:  
  Keywords or tags related to your dApp, such as `"DeFi"`, `"Exchange"`, `"Lending"`. Tags improve searchability within wallets.

- **`version`** *(string, required)*:  
  The version of your dApp metadata, following semantic versioning (e.g., `"1.0.0"`). Update this whenever you make changes to your metadata.

## How to Contribute

We welcome contributions from the Stellar community! Adding your dApp to this repository helps increase its visibility and reach within the Nobak ecosystem.

### Adding Your dApp

1. **Fork the Repository**  
   Click on the "Fork" button in the top-right corner to create a copy of this repository under your GitHub account.

2. **Clone Your Fork**  
   Clone your forked repository to your local machine:

   ```bash
   git clone https://github.com/nobak-net/metadata.git
   ```

3. **Create a New Directory for Your dApp**  
   Navigate into the cloned repository and create a new directory named after your dApp (use kebab-case for multi-word names):

   ```bash
   cd nobak-dapp-metadata
   mkdir my-stellar-dapp-name
   ```

4. **Create the `metadata.json` File**  
   Inside your dApp's directory, create a `metadata.json` file:

   ```bash
   cd my-stellar-dapp-name
   touch metadata.json
   ```

5. **Populate the `metadata.json` File**  
   Copy the recommended structure into your `metadata.json` file and fill in the details specific to your dApp. Ensure that all required fields are included and accurate.

6. **Validate Your JSON**  
   Use a JSON validator to ensure your `metadata.json` file is properly formatted.

7. **Commit Your Changes**  
   Add and commit your changes with a descriptive message:

   ```bash
   git add stellar-dapp-name/metadata.json
   git commit -m "Add metadata for Stellar DApp Name"
   ```

8. **Push to Your Fork**  

   ```bash
   git push origin main
   ```

9. **Create a Pull Request**  
   Go to your forked repository on GitHub and click on "Compare & pull request". Provide a clear description of your dApp and any relevant information.

10. **Await Review**  
    The maintainers will review your pull request. They may request changes or provide feedback. Please respond promptly to any comments.

### Updating Existing Metadata

If you need to update your dApp's metadata:

1. **Fork and Clone the Repository**  
   If you haven't already, fork and clone the repository.

2. **Navigate to Your dApp's Directory**  

   ```bash
   cd metadata/stellar-dapp-name
   ```

3. **Edit the `metadata.json` File**  
   Make the necessary changes to your metadata.

4. **Update the `version` Field**  
   Increment the `version` number according to semantic versioning guidelines.

5. **Commit and Push Changes**  

   ```bash
   git add metadata.json
   git commit -m "Update metadata for Stellar DApp Name to version X.Y.Z"
   git push origin main
   ```

6. **Create a Pull Request**  
   As before, submit a pull request with a description of the changes made.

### Contribution Guidelines

- **Accuracy and Honesty**  
  Ensure all information is accurate and truthful. Misleading information may lead to rejection.

- **Formatting**  
  - Use proper JSON formatting with indentation (2 spaces).
  - Ensure all URLs are valid and begin with `https://`.

- **Required Fields**  
  - All required fields must be present.
  - Optional fields can be omitted if they are not applicable.

- **Logo Requirements**  
  - Logos should be in PNG format with a transparent background if possible.
  - Recommended dimensions are 256x256 pixels.
  - Host images on a reliable and fast CDN or your official website.

- **Security**  
  Do not include any sensitive or private information in your metadata.

- **Compliance**  
  Ensure your dApp complies with all relevant laws and regulations, including any applicable terms of service.

- **Respectful Communication**  
  Maintain professionalism and respect in all communications.

- **Licensing**  
  By submitting your metadata, you agree that it can be used under the repository's [MIT License](LICENSE).

## License

This repository is licensed under the [MIT License](LICENSE). By contributing to this repository, you agree that your contributions will be licensed under the same terms.

## Contact

If you have any questions, need assistance, or wish to report an issue, please open an issue on GitHub or reach out to the Nobak team:

- **Website**: [https://nobak.net](https://nobak.net)

---

Thank you for contributing to the Nobak DApp ecosystem! Your participation helps grow the Stellar network and provides users with seamless access to innovative decentralized applications.