# Update Subscriber Field with Maildroppa

## Endpoint

- **Method:** `PUT`
- **Path:** `/field-type`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Update Subscriber Field](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataType` | body | `string` | no | Data type of the field. |
| `id` | body | `string` | no | Unique identifier of the field type. |
| `name` | body | `string` | no | Display name of the field type. |
| `optionValues[]` | body | `array` | no | List of allowable option values if the data type supports choices. |
