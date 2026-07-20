# List Teams with Make

Lists the teams in the specified organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams`
- **Base URL:** `https://us2.make.com/api/v2`
- **Official documentation:** [List Teams](https://developers.make.com/api-documentation/api-reference/teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | query | `number` | yes | The ID of the Make organization whose teams should be listed. |
