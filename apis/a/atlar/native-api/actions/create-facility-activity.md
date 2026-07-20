# Create facility activity with Atlar

Creates a facility activity in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/financial-data/v2beta/facilities/{id}/activities`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create facility activity](https://docs.atlar.com/reference/post-financial-data-v2beta-facilities-id-activities)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `type` | body | `string<string>` | yes |
| `amount` | body | `object<string>` | yes |
| `localDate` | body | `date<string>` | yes |
