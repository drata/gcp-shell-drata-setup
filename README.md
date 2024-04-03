# gcp-shell-drata-setup

Shell script to create the Drata Read Only service account.

## Usage

The following steps demonstrate how to connect GCP in Drata when using this script.

1. Open the Cloud Shell Terminal in your GCP account [https://console.cloud.google.com/welcome?cloudshell=true](https://console.cloud.google.com/welcome?cloudshell=true).
2. Open the editor and create a file with `sh` extension in the root directory. i.e. `drata.sh`.
3. Copy the content of the `gcp-drata-script.sh`  from this project and paste it in the newly created file.
4. Go back to the Cloud Shell Terminal and run the following commands.
   1. `chmod -x drata.sh` to give it execution permissions.
   2. `drata.sh` to run the script.
5. After the process finishes, from your editor, download the `drata-key-file.json` file.
6.  Go to the GCP connection drawer for user access review and select Upload File to upload the `drata-json-key-file.json` file.
7.  Select the `Save & Test Connection` button.
<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.15 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_null"></a> [null](#provider\_null) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [null_resource.nope](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |

## Inputs

No inputs.

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_nope"></a> [nope](#output\_nope) | TODO: Remove this and add your own outputs |
| <a name="output_true"></a> [true](#output\_true) | n/a |
<!-- END_TF_DOCS -->