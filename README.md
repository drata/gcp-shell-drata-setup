# gcp-shell-drata-setup

Shell script to create the Drata Read Only service account.

## Usage

The following steps demonstrate how to connect GCP in Drata when using this script.

1. Navigate to the Cloud Shell terminal in your GCP account using the following link: [https://console.cloud.google.com/welcome?cloudshell=true](https://console.cloud.google.com/welcome?cloudshell=true).
2. Click the `Open editor` button at the top of the terminal to navigate to your editor.
3. Create a file with `.sh` extension in the root directory i.e. `drata.sh`.
4. Copy the content of the `gcp-drata-script.sh` from this project and paste it in the newly created file.
5. Click the `Open terminal` button at the top of the editor to navigate back to your terminal, run the following commands.
   1. `chmod +x drata.sh` to give it execution permissions.
   2. `./drata.sh` to run the script.
6. The prompt `Will the service account connect multiple projects? [y/n]` will appear. Respond with `n` if it is desired that the service account should only be added to a single project in your organization.
7. After the process finishes, navigate back to your editor and download the `drata-key-file.json` file.
8. In the Drata app, go to the GCP connection drawer and select Upload File to upload the `drata-key-file.json` file.
9. Select the `Save & Test Connection` button.

## Troubleshooting ⚠️

1. Fixing `FAILED_PRECONDITION: Key creation is not allowed on this service account (type: constraints/iam.disableServiceAccountKeyCreation)` issue.
   * Go to the [IAM Organization Policies](https://console.cloud.google.com/iam-admin/orgpolicies) page.
   * Make sure the project where the service account will be stored is selected (top left in the console).
   * Type `Disable service account key creation` on the `🔽 Filter` bar and select the policy.
   * Click over `📝 MANAGE POLICY` button.
   * Go to `Policy source` and select the `Override parent's policy` option.
   * Scroll down a little and open up the `Enforced` rule.
   * Make sure the `Enforcement` section is `Off`.
   * Click `SET POLICY` to save changes.
   * Run this script again.