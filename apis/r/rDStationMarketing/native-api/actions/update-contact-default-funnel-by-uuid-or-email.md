# Update Contact Default Funnel by UUID or Email with RD Station Marketing

## Endpoint

- **Method:** `PUT`
- **Path:** `/platform/contacts/:identifier::value/funnels/default`
- **Base URL:** `https://api.rd.services`
- **Official documentation:** [Update Contact Default Funnel by UUID or Email](https://developers.rdstation.com/reference/put_platform-contacts-identifier-value-funnels-default)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_owner_email` | body | `string` | no | Email do dono do contato. |
| `identifier` | path | `list<string>` | yes | Identifier type in path (uuid or email). Accepted values: `email`, `uuid`. |
| `lifecycle_stage` | body | `string` | no | Etapa do ciclo de vida. |
| `opportunity` | body | `boolean` | no | Indica se o contato é oportunidade. |
| `value` | path | `string` | yes | Identifier value in path. |
