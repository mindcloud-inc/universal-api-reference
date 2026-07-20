# Update Auto Discovery Suggestion with Port API AI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/ai/entities-auto-discovery/:invocation_id/suggestions/:entity_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Auto Discovery Suggestion](https://docs.port.io/api-reference/update-auto-discovery-invocation-suggestion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint` | body | `string` | no | Suggested blueprint identifier. |
| `entity_identifier` | path | `string` | yes | The entity identifier. |
| `identifier` | body | `string` | no | Suggested entity identifier. |
| `invocation_id` | path | `string` | yes | The auto-discovery invocation identifier. |
| `title` | body | `string` | no | Suggested entity title. |
