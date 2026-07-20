# Get Transaction with mintBlue

Retrieves a transaction from mintBlue.

## Endpoint

- **Method:** `POST`
- **Path:** `/sdk/latest`
- **Base URL:** `https://api.mintblue.com`
- **Official documentation:** [Get Transaction](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#getTransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.txid` | body | `string` | yes | Transaction ID to fetch. |
| `params.secret` | body | `string` | no | Optional secret for decrypting outputs. |
