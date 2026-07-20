# List Website Sessions with FullSession

Retrieves website visitor sessions from FullSession.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions/:customerId/:siteId`
- **Base URL:** `https://app.fullsession.io/v1/external`
- **Official documentation:** [List Website Sessions](https://help.fullsession.io/en/articles/11860251-retrieve-website-sessions-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Unique customer ID from Fullsession Setup. |
| `siteId` | path | `string` | yes | Unique site ID for the selected domain. |
| `startAfter` | query | `number` | no | Optional session timestamp in milliseconds. When provided, use the returned startAfter value to continue pagination. |
