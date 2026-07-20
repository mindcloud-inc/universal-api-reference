# Get a section with Asana

Retrieves a section from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `sections/:section_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a section](https://developers.asana.com/reference/getsection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `section_gid` | path | `string` | yes | Path parameter: section_gid |
