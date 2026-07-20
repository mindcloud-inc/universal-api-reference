# Create Deal with Agile CRM

Creates a new deal in Agile CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/opportunity`
- **Base URL:** `https://mindcloud.agilecrm.com/dev/api`
- **Official documentation:** [Create Deal](https://github.com/agilecrm/rest-api#33-create-deal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `expected_value` | body | `number` | yes | — |
| `milestone` | body | `string` | yes | — |
| `close_date` | body | `date` | no | — |
| `probability` | body | `number` | no | Maximum length: 0. |
| `contact_ids` | body | `list<string>` | no | Send multiple values as a array. |
| `description` | body | `string` | no | — |
