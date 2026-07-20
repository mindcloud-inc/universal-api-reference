# Issue Credential with Hyperstack Certificates

## Endpoint

- **Method:** `POST`
- **Path:** `/credentials/new`
- **Base URL:** `https://api.thehyperstack.com/v1`
- **Official documentation:** [Issue Credential](https://thehyperstack.com/docs/api-guide/create-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_attributes` | body | `object` | yes | Custom credential attributes keyed by custom_-prefixed field names. |
| `group_key` | body | `string` | yes | The credential group key to issue into. |
| `recipient` | body | `object` | yes | Recipient object containing name and email. |
