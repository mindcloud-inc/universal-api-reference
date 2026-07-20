# Get holding activity with Atlar

Retrieves a holding activity from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/financial-data/v2beta/portfolios/{pid}/holdings/{hid}/activities/{id}`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Get holding activity](https://docs.atlar.com/reference/get-financial-data-v2beta-portfolios-pid-holdings-hid-activities-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pid` | path | `string<string>` | yes |
| `hid` | path | `string<string>` | yes |
| `id` | path | `string<string>` | yes |
