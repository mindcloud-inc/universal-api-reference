# Remove Access Codes with ClassMarker

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/accesslists/{access_list_id}.json`
- **Base URL:** `https://api.classmarker.com`
- **Official documentation:** [Remove Access Codes](https://www.classmarker.com/online-testing/docs/api/#delete-access-codes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_list_id` | path | `number` | yes | Numeric ClassMarker access list ID. |
| `accessCodes[]` | body | `array<string>` | yes | Access codes to remove from the access list. ClassMarker allows up to 100 codes per request. |
