# Create File with VSCO Workspace

Creates a new file in VSCO Workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/file`
- **Base URL:** `https://workspace.vsco.co/api/v2`
- **Official documentation:** [Create File](https://workspace.vsco.co/api/#operation/createResourceFile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachedTo[]` | body | `array<object>` | no | — |
| `binaryData` | body | `string` | no | — |
| `createdByContactId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `description` | body | `string` | no | — |
| `filename` | body | `string` | yes | — |
| `imageMetaData` | body | `object` | no | — |
| `mimeType` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `remoteUrl` | body | `string` | no | — |
| `typeId` | body | `string` | no | A ULID entity identifier that is nullable. |
