# Get Contact by UUID or Email with RD Station Marketing

## Endpoint

- **Method:** `GET`
- **Path:** `/platform/contacts/:identifier::value`
- **Base URL:** `https://api.rd.services`
- **Official documentation:** [Get Contact by UUID or Email](https://developers.rdstation.com/reference/get_platform-contacts-identifier-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `list<string>` | yes | Identifier type in path (uuid or email). Accepted values: `email`, `uuid`. |
| `value` | path | `string` | yes | Identifier value in path. |
