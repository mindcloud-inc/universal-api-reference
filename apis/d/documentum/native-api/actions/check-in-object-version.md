# Check In Object Version with Documentum

## Endpoint

- **Method:** `POST`
- **Path:** `/repositories/{repositoryName}/objects/{chronicleId}/versions`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Check In Object Version](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `chronicleId` | path | `string` | yes | Chronicle ID of the object being checked in. |
| `objectid` | query | `string` | yes | Current object ID being checked in. |
| `version-policy` | query | `string` | yes | Versioning policy: next-major, next-minor, branch-version, or same-version. |
| `properties` | body | `object` | no | Optional JSON properties payload for the check-in. |
