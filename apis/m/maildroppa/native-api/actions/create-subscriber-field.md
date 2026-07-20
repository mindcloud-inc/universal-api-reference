# Create Subscriber Field with Maildroppa

## Endpoint

- **Method:** `POST`
- **Path:** `/field-type`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Create Subscriber Field](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataType` | body | `string` | no | Data type of the field. |
| `name` | body | `string` | no | Display name of the field type. |
| `optionValues[]` | body | `array` | no | List of allowable option values if the data type supports choices. |
