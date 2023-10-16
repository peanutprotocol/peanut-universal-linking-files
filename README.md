# Universal Linking Configuration Repository

This repository contains two essential configuration files within the `src` folder: `apple-app-site-association` and `assetLinks.json`. These files are used to enable Universal Linking for the peanut.to domain, allowing users to seamlessly transition from a website to a mobile application.

## Contributing

To enable Universal Linking for your mobile application on peanut.to, you can make a Pull Request (PR) to this repository. Here's what you need to do:

### Updating the AASA File

The `apple-app-site-association` (AASA) file must be updated with the `teamId` and `bundleId` of your mobile app. You can find these values in your app's settings. Follow these steps:

1. **Find Your `teamId`:**

   - Go to your Apple Developer Account.
   - Navigate to "Membership."
   - Your `teamId` can be found under the team name.

2. **Find Your `bundleId`:**

   - In your Xcode project project, locate the app's bundle identifier. It usually follows a format like `com.companyname.appname`.

3. **Update the AASA File:**
   - Edit the `apple-app-site-association` file in this repository.
   - make a new entry with the `teamId` and `bundleId` fields with your own values.
   - Save the file.

### Updating the assetLinks.json File

The `assetLinks.json` file must be updated with the package name and SHA256 fingerprints of your mobile app. You can find these values in your app's settings. Follow these steps:

1. **Find Your Package Name:**

   - For Android, the package name is specified in the `build.gradle` file.

2. **Find Your SHA256 Fingerprints:**

   - Generate SHA256 fingerprints for your app's signing certificate(s).

3. **Update the assetLinks.json File:**
   - Edit the `assetLinks.json` file in this repository.
   - make a new entry with the `"package_name"` and `"sha256_cert_fingerprints"` fields with your own values.
   - Save the file.

### Submitting a Pull Request

1. Fork this repository to your GitHub account.

2. Clone your forked repository to your local machine:

   ```shell
   git clone https://github.com/your-username/universal-linking-config.git
   ```

3. Create a new branch for your changes:

   ```shell
   git checkout -b feature/your-feature-name
   ```

4. Make the necessary updates to the AASA and assetLinks.json files.

5. Commit your changes:

   ```shell
   git add .
   git commit -m "Update AASA and assetLinks.json for my mobile app"

   ```

6. Push your changes to your forked repository:

   ```shell
   git push origin feature/your-feature-name

   ```

7. Create a Pull Request from your forked repository to this repository.

Once your PR is reviewed and accepted, Universal Linking will be configured for your mobile application on peanut.to.

For more detailed information and troubleshooting tips, please refer to our [Universal Linking Documentation](https://docs.peanut.to/integrations/universal-linking).

If you have any questions or need assistance, feel free to reach out to us in our [Discord](https://discord.com/invite/BX9Ak7AW28).
