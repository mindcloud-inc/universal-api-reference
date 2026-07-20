# Review Auto Discovery Suggestions with Port API AI

Reviews auto-discovery suggestions in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai/entities-auto-discovery/:invocation_id/review`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Review Auto Discovery Suggestions](https://docs.port.io/api-reference/review-auto-discovery-invocation-suggestions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkAction` | body | `object` | yes | Bulk review action object. |
| `invocation_id` | path | `string` | yes | The auto-discovery invocation identifier. |
