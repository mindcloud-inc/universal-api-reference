# Get Feed URL with Beamer

Retrieves the Beamer feed URL for a user.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/url`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Get Feed URL](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | query | `string` | no | Retrieve the feed URL in a specific language. |
| `filterByUrl` | query | `boolean` | no | Apply URL filtering to the feed. |
| `filter` | query | `string` | no | Retrieve posts with a matching segmentation filter. |
| `forceFilter` | query | `string` | no | Only retrieve posts that match this segmentation filter. |
| `userFirstName` | query | `string` | no | First name of the user viewing the feed. |
| `userLastName` | query | `string` | no | Last name of the user viewing the feed. |
| `userEmail` | query | `string` | no | Email of the user viewing the feed. |
| `userId` | query | `string` | no | ID of the user viewing the feed. |
| `theme` | query | `string` | no | Feed theme to use in the generated URL. |
