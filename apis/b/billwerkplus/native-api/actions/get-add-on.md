# Get Add-On with Billwerkplus

Retrieves an add-on from Billwerkplus.

## Endpoint

- **Method:** `GET`
- **Path:** `/add_on/:handle`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [Get Add-On](https://docs.frisbii.com/reference/getaddon)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | path | `string` | yes | Add-on handle. |
| `tax_rate_for_country` | query | `string` | no | Country code to evaluate tax rate for. |
