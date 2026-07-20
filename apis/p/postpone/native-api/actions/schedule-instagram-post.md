# Schedule Instagram Post with Postpone

Schedules an Instagram post in Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [Schedule Instagram Post](https://developers.postpone.app/scheduling-posts/platforms/instagram)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.username` | body | `string` | yes | The username of the connected Instagram account to post from. |
| `variables.input.caption` | body | `string` | no | The main caption for the Instagram post. |
| `variables.input.mediaUrl` | body | `string` | yes | URL of media to upload and attach to the post. |
| `variables.input.submissions[].postAt` | body | `string` | yes | When to publish the content in ISO 8601 format. |
| `variables.input.submissions[].mediaType` | body | `string` | yes | Type of Instagram content to schedule. |
