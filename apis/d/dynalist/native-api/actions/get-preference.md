# Get Preference with Dynalist

Retrieves a preference value from Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/pref/get`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Get Preference](https://apidocs.dynalist.io/#get-preference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Preference key to read, such as `inbox_location` or `inbox_position`. |
