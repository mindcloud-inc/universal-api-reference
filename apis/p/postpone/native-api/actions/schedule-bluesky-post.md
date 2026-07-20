# Schedule Bluesky Post with Postpone

Schedules a Bluesky post in Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [Schedule Bluesky Post](https://developers.postpone.app/scheduling-posts/platforms/bluesky)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.username` | body | `string` | yes | The username of the connected Bluesky account to post from. |
| `variables.input.postAt` | body | `string` | yes | When to publish the post in ISO 8601 format. |
| `variables.input.thread[].text` | body | `string` | yes | The post text content for each item in the thread. |
| `variables.input.thread[].order` | body | `number` | yes | The 0-based position of each post in the thread. |
| `variables.input.thread[].contentWarning` | body | `string` | yes | The content warning label for each post in the thread. |
