# Get Artefact with Vouchsafe

Retrieves an artefact download link from Vouchsafe.

## Endpoint

- **Method:** `GET`
- **Path:** `/artefacts/:artefact_key`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Get Artefact](https://app.vouchsafe.id/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `artefact_key` | path | `string` | yes | The artefact key to exchange for a presigned download URL. |
