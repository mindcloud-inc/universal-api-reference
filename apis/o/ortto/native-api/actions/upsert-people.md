# Upsert People with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/person/merge`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Upsert People](https://help.ortto.com/a-257-create-or-update-one-or-more-people-merge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `people[]` | body | `array<object>` | yes | One or more people to create or update in Ortto. Each item should include a fields object and may include tags or unset_tags. |
| `merge_by[]` | body | `array<string>` | no | Identifiers Ortto should use to match existing people, such as str::email. |
| `async` | body | `boolean` | no | Whether Ortto should process the merge asynchronously. |
| `merge_strategy` | body | `number` | no | Ortto merge strategy value to use when matching contacts. |
| `find_strategy` | body | `number` | no | Ortto find strategy value to use when creating contacts. |
