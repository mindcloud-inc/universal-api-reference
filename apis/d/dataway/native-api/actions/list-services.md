# List Services with Dataway

Retrieves available services from Dataway for a selected category.

## Endpoint

- **Method:** `GET`
- **Path:** `/get-services`
- **Base URL:** `https://datawayapp.com/vendor`
- **Official documentation:** [List Services](https://documenter.getpostman.com/view/421216/UV5Ukz4U)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | yes | Service category slug, for example airtime or data. |
