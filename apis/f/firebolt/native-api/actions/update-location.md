# Update Location with Firebolt

Updates an existing location in Firebolt.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:engineHost`
- **Base URL:** `https://api.app.firebolt.io`
- **Official documentation:** [Update Location](https://docs.firebolt.io/reference-sql/commands/data-definition/alter-location)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engineHost` | path | `string` | yes | System engine host to execute the ALTER LOCATION statement against. |
| `locationName` | body | `string` | yes | The Firebolt location object to alter. |
| `alterClause` | body | `string` | yes | The ALTER LOCATION clause, for example SET URL = 's3://bucket/new-prefix/' or RENAME TO new_location_name. |
