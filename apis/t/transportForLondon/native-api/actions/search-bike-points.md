# Search Bike Points with Transport for London

Finds bike points in Transport for London by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/BikePoint/Search`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Search Bike Points](https://api.tfl.gov.uk/swagger/ui/index.html#!/BikePoint/BikePoint_Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Bike point search text, such as street or landmark name. |
