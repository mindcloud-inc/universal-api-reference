# Create Account Custom Field with Fliqr AI

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/custom_fields`
- **Base URL:** `https://app.fliqr.ai/api/`
- **Official documentation:** [Create Account Custom Field](https://docs.fliqr.ai/api-reference/accounts/post-accountscustom-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Custom field name. |
| `type` | body | `number` | no | Custom field type: 0 text, 1 number, 2 date, 3 datetime, 4 boolean. |
| `isBotField` | body | `boolean` | no | Whether this is a bot field. |
| `value` | body | `string` | no | Bot field value; ignored for user custom fields. |
| `description` | body | `string` | no | Custom field description. |
