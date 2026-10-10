# Add Records to a List with Apollo

## Endpoint

- **Method:** `POST`
- **Path:** `v1/labels/add_entity_ids_to_label_names`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Add Records to a List](https://docs.apollo.io/reference/add-records-to-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_ids[]` | body | `array<string>` | yes | — |
| `label_names[]` | body | `array<string>` | yes | — |
| `modality` | body | `list<string>` | yes | Accepted values: `accounts`, `contacts`. |
| `async` | body | `boolean` | no | — |
