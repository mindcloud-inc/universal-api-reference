# Set Preference with Dynalist

Updates a preference value in Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/pref/set`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Set Preference](https://apidocs.dynalist.io/#set-preference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Preference key to update. |
| `value` | body | `string` | yes | New preference value. |
