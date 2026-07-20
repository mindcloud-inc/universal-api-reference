# Add Tag to Contact by UUID or Email with RD Station Marketing

## Endpoint

- **Method:** `POST`
- **Path:** `/platform/contacts/:identifier::value/tag`
- **Base URL:** `https://api.rd.services`
- **Official documentation:** [Add Tag to Contact by UUID or Email](https://developers.rdstation.com/reference/post_platform-contacts-identifier-value-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `list<string>` | yes | Identifier type in path (uuid or email). Accepted values: `email`, `uuid`. |
| `tags[]` | body | `array<string>` | yes | Tags a serem adicionadas ao contato. |
| `value` | path | `string` | yes | Identifier value in path. |
