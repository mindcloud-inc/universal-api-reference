# Rename Design with PostcardMania

Updates an existing design in PostcardMania.

## Endpoint

- **Method:** `PUT`
- **Path:** `/design/{{designID}}`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Rename Design](https://docs.pcmintegrations.com/docs/directmail-api/3eg5izp9nvj8m)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `designID` | path | `string` | no | The design identifier to update. |
| `friendlyName` | body | `string` | no | New design name. |
