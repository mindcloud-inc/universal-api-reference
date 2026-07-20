# Schedule Pinterest Post with Postpone

Schedules a Pinterest post in Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [Schedule Pinterest Post](https://developers.postpone.app/scheduling-posts/platforms/pinterest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.username` | body | `string` | yes | The username of the connected Pinterest account to post from. |
| `variables.input.title` | body | `string` | yes | The title of the Pinterest pin. |
| `variables.input.description` | body | `string` | no | The description for the Pinterest pin. |
| `variables.input.link` | body | `string` | no | The URL the Pinterest pin should link to. |
| `variables.input.mediaUrl` | body | `string` | yes | URL of an image to upload and use for the pin. |
| `variables.input.boardId` | body | `string` | yes | The Pinterest board ID to pin to. |
| `variables.input.submissions[].postAt` | body | `string` | yes | When to publish the pin in ISO 8601 format. |
