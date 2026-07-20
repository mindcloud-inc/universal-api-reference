# Schedule LinkedIn Post with Postpone

Schedules a LinkedIn post in Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [Schedule LinkedIn Post](https://developers.postpone.app/scheduling-posts/platforms/linkedin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.username` | body | `string` | yes | The username of the connected LinkedIn account to post from. |
| `variables.input.text` | body | `string` | yes | The main text content of the LinkedIn post. |
| `variables.input.visibility` | body | `string` | yes | The visibility setting for the LinkedIn post. |
| `variables.input.submissions[].postAt` | body | `string` | yes | When to publish the content in ISO 8601 format. |
