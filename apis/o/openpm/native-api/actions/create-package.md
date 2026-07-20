# Create Package with openpm

## Endpoint

- **Method:** `POST`
- **Path:** `/packages`
- **Base URL:** `https://openpm.ai/api`
- **Official documentation:** [Create Package](https://openpm.ai/apis/openpm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Package ID. |
| `name` | body | `string` | no | Package name. |
| `machine_name` | body | `string` | no | Package name for machines. |
| `domain` | body | `string` | no | Package domain. |
| `version` | body | `string` | no | Package version. |
| `logo_url` | body | `string` | no | Package logo URL. |
| `contact_email` | body | `string` | no | Package contact email. |
| `legal_info_url` | body | `string` | no | Package legal info URL. |
| `description` | body | `string` | no | Package description. |
| `machine_description` | body | `string` | no | Package description for machines. |
| `openapi` | body | `string` | yes | Package OpenAPI specification. Runtime validation requires the OpenAPI document to include a server URL/domain. |
