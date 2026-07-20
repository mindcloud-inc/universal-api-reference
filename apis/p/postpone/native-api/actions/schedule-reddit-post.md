# Schedule Reddit Post with Postpone

Schedules a Reddit post in Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [Schedule Reddit Post](https://developers.postpone.app/scheduling-posts/platforms/reddit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.username` | body | `string` | yes | The username of the connected Reddit account to post from. |
| `variables.input.title` | body | `string` | yes | The title of the Reddit post. |
| `variables.input.content` | body | `string` | yes | The text content for the Reddit post. |
| `variables.input.submissions[].validationId` | body | `string` | yes | Internal submission identifier used for validation mapping. |
| `variables.input.submissions[].subreddit` | body | `string` | yes | The subreddit name without the r/ prefix. |
| `variables.input.submissions[].postAt` | body | `string` | yes | When to publish the content in ISO 8601 format. |
