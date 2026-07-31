# List squirrel sightings with NYC Squirrel Census

## Endpoint

- **Method:** `GET`
- **Path:** `/resource/vfnx-vebw.json`
- **Base URL:** `https://data.cityofnewyork.us`
- **Official documentation:** [List squirrel sightings](https://dev.socrata.com/foundry/data.cityofnewyork.us/vfnx-vebw)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$where` | query | `string` | no | Optional advanced SoQL predicate for the fixed NYC Squirrel Census dataset. For example: primary_fur_color = 'Gray'. |
