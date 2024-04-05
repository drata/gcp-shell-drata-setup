# gcp-shell-drata-setup

Shell script to create the Drata Read Only service account.

## Usage

The following steps demonstrate how to connect GCP in Drata when using this script.

1. Navigate to the Cloud Shell terminal in your GCP account using the following link: [https://console.cloud.google.com/welcome?cloudshell=true](https://console.cloud.google.com/welcome?cloudshell=true).
2. Click the `Open editor` button at the top of the terminal to navigate to your editor.
3. Create a file with `.sh` extension in the root directory i.e. `drata.sh`.
4. Copy the content of the `gcp-drata-script.sh` from this project and paste it in the newly created file.
5. Click the `Open terminal` button at the top of  the editor to navigate back to your terminal, run the following commands.
   1. `chmod +x drata.sh` to give it execution permissions.
   2. `./drata.sh` to run the script.
6. After the process finishes, navigate back to your editor and download the `drata-key-file.json` file.
7. In the Drata app, go to the GCP connection drawer and select Upload File to upload the `drata-key-file.json` file.
8. Select the `Save & Test Connection` button.