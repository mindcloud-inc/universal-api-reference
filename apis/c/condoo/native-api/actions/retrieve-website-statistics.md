# Retrieve Website Statistics with condoo

Retrieves website statistics from condoo.

## Endpoint

- **Method:** `GET`
- **Path:** `/statistics/{website_id}`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [Retrieve Website Statistics](https://trk.condoo.systems/en/api-documentation/statistics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Optional country code. |
| `end_date` | query | `date` | yes | Required end date. |
| `start_date` | query | `date` | yes | Required start date. |
| `type` | query | `string` | no | Optional statistics type. |
| `utm_source` | query | `string` | no | Optional UTM source for supported UTM statistics types. |
| `website_id` | path | `number` | yes | Required website ID. |
