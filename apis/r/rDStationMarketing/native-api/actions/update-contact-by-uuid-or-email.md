# Update Contact by UUID or Email with RD Station Marketing

## Endpoint

- **Method:** `PATCH`
- **Path:** `/platform/contacts/:identifier::value`
- **Base URL:** `https://api.rd.services`
- **Official documentation:** [Update Contact by UUID or Email](https://developers.rdstation.com/reference/patch_platform-contacts-identifier-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bio` | body | `string` | no | Anotações sobre contato. |
| `birthdate` | body | `string` | no | Data de aniversário. |
| `city` | body | `string` | no | Cidade do contato. |
| `country` | body | `string` | no | País do contato. |
| `email` | body | `string` | no | Email do contato. |
| `facebook` | body | `string` | no | Facebook do contato. |
| `identifier` | path | `list<string>` | yes | Identifier type in path (uuid or email). Accepted values: `email`, `uuid`. |
| `job_title` | body | `string` | no | Cargo do contato. |
| `legal_bases[]` | body | `array<object>` | no | Bases legais do contato. |
| `legal_bases[].category` | body | `list<string>` | no | Categoria da base legal (ex.: communications). Accepted values: `communications`, `data_processing`. |
| `legal_bases[].status` | body | `list<string>` | no | Status da base legal (ex.: granted). Accepted values: `declined`, `granted`. |
| `legal_bases[].type` | body | `list<string>` | no | Tipo da base legal (ex.: consent). Accepted values: `consent`, `judicial_process`, `legitimate_interest`, `pre_existent_contract`, `public_interest`, `vital_interest`. |
| `linkedin` | body | `string` | no | LinkedIn do contato. |
| `mobile_phone` | body | `string` | no | Celular do contato. |
| `name` | body | `string` | no | Nome do contato. |
| `personal_phone` | body | `string` | no | Telefone do contato. |
| `state` | body | `string` | no | Estado do contato. |
| `tags[]` | body | `array<string>` | no | Tags do contato. |
| `twitter` | body | `string` | no | Twitter do contato. |
| `value` | path | `string` | yes | Identifier value in path. |
| `website` | body | `string` | no | Site do contato. |
