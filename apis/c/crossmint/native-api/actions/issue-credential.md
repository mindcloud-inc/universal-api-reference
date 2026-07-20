# Issue Credential with Crossmint

Issues a credential in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1-alpha1/credentials/templates/:templateId/vcs`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Issue Credential](https://docs.crossmint.com/api-reference/verifiable-credentials/credentials/issue-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Credential template identifier related to the new credential. |
| `recipient` | body | `string` | yes | Recipient address in `<chain>:<address>` or `email:<email_address>:<chain>` format. |
| `credential` | body | `object` | yes | Credential payload object. Include `subject` and optional `expiresAt`. |
| `sendNotification` | body | `boolean` | no | Notify the recipient by email after issuance. Defaults to true. |
| `locale` | body | `string` | no | Locale for notification content. Defaults to `en-US`. |
| `metadata` | body | `object` | no | Optional credential NFT metadata override object. |
