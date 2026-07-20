# Get Restlet with NetSuite - Advanced

## Endpoint

- **Method:** `GET`
- **Path:** `https://{accountId}.restlets.api.netsuite.com/app/site/hosting/restlet.nl`
- **Base URL:** `https://{accountId}.suitetalk.api.netsuite.com`
- **API:** REST

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `script` | query | `string` | no |
| `deploy` | query | `string` | no |
| `searchId` | query | `string` | no |
| `expandSubResources` | query | `boolean` | no |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
| `filter` | query | `string` | no |
| `sort` | query | `string` | no |
| `rawFilter` | query | `string` | no |
| `columns` | query | `string` | no |
| `type` | query | `string` | no |
