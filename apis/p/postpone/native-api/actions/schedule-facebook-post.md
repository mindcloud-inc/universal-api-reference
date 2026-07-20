# Schedule Facebook Post with Postpone

Schedules a Facebook post in Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [Schedule Facebook Post](https://developers.postpone.app/scheduling-posts/platforms/facebook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.username` | body | `string` | yes | The username of the connected Facebook account to post from. |
| `variables.input.text` | body | `string` | no | The main text content of the Facebook post. |
| `variables.input.submissions[].postAt` | body | `string` | yes | When to publish the content in ISO 8601 format. |
| `variables.input.submissions[].mediaType` | body | `string` | yes | Type of Facebook content to schedule. |
