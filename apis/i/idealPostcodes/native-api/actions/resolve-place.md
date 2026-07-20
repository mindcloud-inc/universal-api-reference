# Resolve Place with Ideal Postcodes

Retrieves a place from Ideal Postcodes by place ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/places/:place`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Resolve Place](https://docs.ideal-postcodes.co.uk/docs/api/resolve-place)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `place` | path | `string` | yes | Place suggestion ID to resolve. |
| `tags` | query | `string` | no | Comma-separated tags to associate with the resolution request. |
