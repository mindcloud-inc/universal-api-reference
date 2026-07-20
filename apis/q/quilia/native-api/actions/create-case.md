# Create Case with Quilia

## Endpoint

- **Method:** `POST`
- **Path:** `cases`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [Create Case](https://api.quilia.dev/v2#tag/cases/POST/cases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | no | The ID of an existing client |
| `cms_type` | body | `string` | no | Look up integration by CMS type when ID is absent |
| `native_id` | body | `string` | no | The native ID of the case in the external system. Used for integration and idempotency. |
| `new_client` | body | `object` | no | The client to associate with the case |
| `new_client.email` | body | `string` | no | The email of the client |
| `new_client.language_code` | body | `string` | no | The language code of the client |
| `new_client.name` | body | `string` | no | The name of the client |
| `new_client.name_first` | body | `string` | no | The first name of the client |
| `new_client.name_last` | body | `string` | no | The last name of the client |
| `new_client.phone` | body | `string` | no | The phone number of the client |
| `organization_integration_id` | body | `string` | no | The ID of the organization integration to use |
| `phase` | body | `string` | no | The current phase of the case |
| `type` | body | `string` | yes | The type of the case. Can be a Quilia case type or a custom CMS case type that will be mapped via integration settings. |
| `status` | body | `list<string>` | no | The status of the case Accepted values: `closed`, `open`, `pending`. |
| `opened_at` | body | `date` | no | The date and time when the case was opened |
| `created_at` | body | `date` | no | The date and time when the case was created |
| `updated_at` | body | `date` | no | The date and time when the case was last updated |
