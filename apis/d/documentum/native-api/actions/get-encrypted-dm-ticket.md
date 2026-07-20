# Get Encrypted DM Ticket with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/dm-ticket`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Get Encrypted DM Ticket](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `secure` | query | `boolean` | no | Set to true to request an encrypted DM ticket. |
