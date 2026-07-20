# List Access Tokens with Testlify

Retrieves Testlify access tokens with optional filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/workspace/accesstokens`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [List Access Tokens](https://docs.testlify.com/reference/get_access_tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search text for access tokens. |
| `createdBy` | query | `string` | no | Filter by creator. |
| `status` | query | `string` | no | Filter by token status. |
