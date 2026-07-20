# Plan Journey with Transport for London

Plans a journey between locations in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/Journey/JourneyResults/:from/to/:to`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Plan Journey](https://api.tfl.gov.uk/swagger/ui/index.html#!/Journey/Journey_JourneyResults)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | path | `string` | yes | Journey origin: coordinates, postcode, Naptan ID, Stop ID, or free text. |
| `to` | path | `string` | yes | Journey destination: coordinates, postcode, Naptan ID, Stop ID, or free text. |
| `mode` | query | `string` | no | Optional comma-separated journey modes, such as tube,bus,walking. |
| `date` | query | `string` | no | Optional journey date in yyyyMMdd format. |
| `time` | query | `string` | no | Optional journey time in HHmm format. |
