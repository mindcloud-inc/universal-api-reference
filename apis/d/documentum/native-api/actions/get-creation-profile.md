# Get Creation Profile with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/profile-configuration/{profileId}`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Get Creation Profile](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `profileId` | path | `string` | yes | Object ID of the D2 creation profile. |
