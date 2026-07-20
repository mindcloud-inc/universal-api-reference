# Get Single Feed with Zoho Connect

Retrieves a single feed from Zoho Connect.

## Endpoint

- **Method:** `GET`
- **Path:** `/pulse/api/v1/singleStream`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Get Single Feed](https://www.zoho.com/connect/api/get-single-feed.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | ID of the network where the post was made. |
| `streamId` | query | `string` | yes | The post to fetch by ID. |
| `streamUrl` | query | `string` | no | Optional post URL to fetch the post instead of the ID. |
| `commentIndex` | query | `number` | no | Start index for comments. The default is 0. |
| `commentLimit` | query | `number` | no | Set a limit on the number of comments. The default is 20. |
| `isThread` | query | `boolean` | no | Set to true for threaded comments, or false for normal view. |
| `needAllComments` | query | `boolean` | no | Set to true to return all comments. |
