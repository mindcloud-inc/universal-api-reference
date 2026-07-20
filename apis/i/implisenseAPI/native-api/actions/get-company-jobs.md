# Get Company Jobs with Implisense

Retrieves company jobs from Implisense API.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:id/jobs`
- **Base URL:** `https://german-company-data.p.rapidapi.com`
- **Official documentation:** [Get Company Jobs](https://docs.implisense.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Implisense company identifier, for example DEVFCLQFW054. |
| `since` | query | `string` | no | Optional lower timestamp boundary for returned jobs. |
| `size` | query | `number` | no | Maximum number of jobs to return. |
