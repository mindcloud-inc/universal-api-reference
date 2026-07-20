# List Keywords with AppFollow

Retrieves keyword data from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/aso/keywords`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [List Keywords](https://docs.api.appfollow.io/reference/keywords_api_v2_aso_keywords_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | yes | App external ID. |
| `country` | query | `string` | no | Country code. |
| `device` | query | `string` | no | Device type. |
| `date` | query | `string` | no | Date. |
