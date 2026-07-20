# Delete Contact by UUID or Email with RD Station Marketing

## Endpoint

- **Method:** `DELETE`
- **Path:** `/platform/contacts/:identifier::value`
- **Base URL:** `https://api.rd.services`
- **Official documentation:** [Delete Contact by UUID or Email](https://developers.rdstation.com/reference/delete_platform-contacts-identifier-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `list<string>` | yes | Identifier type in path (uuid or email). Accepted values: `email`, `uuid`. |
| `value` | path | `string` | yes | Identifier value in path. |
