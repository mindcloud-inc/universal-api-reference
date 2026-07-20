# Update Credential with Hyperstack Certificates

## Endpoint

- **Method:** `POST`
- **Path:** `/credential/:document_id/update`
- **Base URL:** `https://api.thehyperstack.com/v1`
- **Official documentation:** [Update Credential](https://thehyperstack.com/docs/api-guide/update-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The credential document identifier. |
| `expiry` | body | `number` | yes | Unix timestamp in seconds for the new expiry date. |
