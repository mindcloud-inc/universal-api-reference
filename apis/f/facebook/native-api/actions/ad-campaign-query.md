# Ad Campaign Query with Facebook

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountID`
- **Base URL:** `https://graph.facebook.com/v25.0`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountID` | path | `string` | yes | The Meta ad account ID, including the act_ prefix. |
| `fields` | query | `string` | no | Send multiple values as a array. |
