# Create Blacklist Entry with NobelSMS

Creates a new blacklist entry in NobelSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/black_list`
- **Base URL:** `https://api.nobelsms.com/rest`
- **Official documentation:** [Create Blacklist Entry](https://api.nobelsms.com/rest/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bnumber` | body | `number` | yes | B-number. |
| `tag_id` | body | `number` | no | Tag ID. |
