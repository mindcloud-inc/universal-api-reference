# Schedule Threads Post with Postpone

Schedules a Threads post in Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [Schedule Threads Post](https://developers.postpone.app/scheduling-posts/platforms/threads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.username` | body | `string` | yes | The username of the connected Threads account to post from. |
| `variables.input.postAt` | body | `string` | yes | When to publish the post in ISO 8601 format. |
| `variables.input.thread[].text` | body | `string` | yes | The post text content for each item in the thread. |
| `variables.input.thread[].order` | body | `number` | yes | The 0-based position of each post in the thread. |
