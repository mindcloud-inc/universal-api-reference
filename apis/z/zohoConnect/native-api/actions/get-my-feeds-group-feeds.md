# Get My Feeds & Group Feeds with Zoho Connect

Retrieves your feeds and group feeds from Zoho Connect.

## Endpoint

- **Method:** `GET`
- **Path:** `/pulse/api/getLatestStreams`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Get My Feeds & Group Feeds](https://www.zoho.com/connect/api/get-my-feed-group-feed.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | ID of the network where the posts were made. |
| `partitionId` | query | `string` | no | Optional group ID to narrow the feed to a specific group wall. |
| `lastViewedTime` | query | `number` | yes | Fetch posts after this timestamp, in milliseconds. |
| `streamLimit` | query | `number` | no | Set a limit for the posts. |
| `fetchTime` | query | `number` | no | Fetch posts up to this timestamp, in milliseconds. |
