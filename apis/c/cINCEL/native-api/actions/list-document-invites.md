# List Document Invites with CINCEL

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team/folders/:folder/documents/:document/invites`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [List Document Invites](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders/-folder-/documents/-document-/invites)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | Team UUID from the path. |
| `folder` | path | `string` | yes | Folder UUID from the path. |
| `document` | path | `string` | yes | Document UUID from the path. |
| `include_deleted` | query | `boolean` | no | Include deleted invites. |
| `name_like` | query | `string` | no | Filter invites by name substring. |
