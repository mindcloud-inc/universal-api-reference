# Get RCS Capabilities with Seven

Retrieves RCS capabilities from Seven.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/rcs`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Get RCS Capabilities](https://docs.seven.io/en/rest-api/endpoints/lookup#rcs-capabilities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | The number to be queried. Multiple numbers must be separated by commas. You can enter almost any format; the API formats the number automatically. |
| `from` | query | `string` | no | To check the RCS capabilities of a phone number, the respective agent identifier is always required. By default, our API uses the first RCS sender ID in your account. You can use a different agent with this parameter. |
