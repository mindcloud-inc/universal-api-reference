# Update Test Browsers with Headless Testing

Updates browser assignments for a codeless test in Headless Testing.

## Endpoint

- **Method:** `POST`
- **Path:** `/lab/:id/browsers`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Update Test Browsers](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `browser_ids` | body | `string` | yes | Comma-separated browser IDs to assign to the codeless test. |
| `id` | path | `string` | yes | The codeless test identifier. |
