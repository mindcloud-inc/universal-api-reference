# Get Timestamp Or Certificate Artifact with CINCEL

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team/folders/:folder/documents/:document/:timestamp`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Get Timestamp Or Certificate Artifact](https://docs.cincel.digital/v3/digital-signature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | Team UUID from the path. |
| `folder` | path | `string` | yes | Folder UUID from the path. |
| `document` | path | `string` | yes | Document UUID from the path. |
| `timestamp` | path | `string` | yes | Artifact name such as `timestamp.tsr`, `timestamp.asn1`, `timestamp.xml`, or `timestamp.pdf`. |
