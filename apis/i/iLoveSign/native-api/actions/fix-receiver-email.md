# Fix Receiver Email with iLoveSign

## Endpoint

- **Method:** `PUT`
- **Path:** `/signature/receiver/fix-email/:receiver_token_requester`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Fix Receiver Email](https://www.iloveapi.com/docs/api-reference#fix-signer-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `receiver_token_requester` | path | `string` | yes | Receiver token requester identifier. |
| `email` | body | `string` | yes | Replacement email address for the receiver. |
