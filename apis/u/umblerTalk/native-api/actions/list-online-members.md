# List Online Members with Umbler Talk

Retrieves online members from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/members/online/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [List Online Members](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | query | `string` | yes | The organization ID. Use Get Current Member to find available organizations. |
