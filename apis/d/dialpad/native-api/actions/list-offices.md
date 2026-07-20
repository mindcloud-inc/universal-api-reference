# List Offices with Dialpad

Retrieves accessible office records from Dialpad.

## Endpoint

- **Method:** `GET`
- **Path:** `/offices`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [List Offices](https://developers.dialpad.com/reference/officeslist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active_only` | query | `boolean` | no | Whether we only return active offices. |
| `cursor` | query | `string` | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |
