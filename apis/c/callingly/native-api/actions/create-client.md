# Create Client with Callingly

Creates a client in Callingly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/clients`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Create Client](https://help.callingly.com/article/38-callingly-api-documentation#create-client)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fname` | body | `string` | yes |
| `lname` | body | `string` | yes |
| `company` | body | `string` | yes |
| `email` | body | `string` | yes |
| `phone_number` | body | `string` | yes |
| `password` | body | `string` | no |
