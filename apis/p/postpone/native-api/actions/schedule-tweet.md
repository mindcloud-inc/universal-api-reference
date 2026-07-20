# Schedule Tweet with Postpone

Schedules a tweet in Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [Schedule Tweet](https://developers.postpone.app/scheduling-posts/platforms/twitter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.username` | body | `string` | yes | The username of the connected X/Twitter account to post from. |
| `variables.input.postAt` | body | `string` | yes | When to publish the tweet in ISO 8601 format. |
| `variables.input.thread[].text` | body | `string` | yes | The tweet text content for each item in the thread. |
| `variables.input.thread[].order` | body | `number` | yes | The 0-based position of each tweet in the thread. |
