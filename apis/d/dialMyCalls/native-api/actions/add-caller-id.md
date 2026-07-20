# Add Caller ID with DialMyCalls

Creates a new caller ID in DialMyCalls.

## Endpoint

- **Method:** `POST`
- **Path:** `/callerid`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Add Caller ID](https://www.dialmycalls.com/api-documentation#callerid-add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The caller ID's name. |
| `phone` | body | `string` | yes | The caller ID phone number. |
