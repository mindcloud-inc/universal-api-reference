# Set Filters with Syften

Updates the saved filter list in Syften.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/0.0/filters/set`
- **Base URL:** `https://syften.com`
- **Official documentation:** [Set Filters](https://github.com/syften/syften-examples/blob/master/curl/filters_set.sh)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[]` | body | `array<string>` | yes | Complete filter list to store in Syften |
