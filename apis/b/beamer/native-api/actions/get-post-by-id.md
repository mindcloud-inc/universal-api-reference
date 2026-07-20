# Get Post By ID with Beamer

Retrieves a post from Beamer by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/posts/:postId`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Get Post By ID](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postId` | path | `number` | yes | ID of the post to retrieve. |
| `userFirstName` | query | `string` | no | — |
| `userLastName` | query | `string` | no | — |
| `userEmail` | query | `string` | no | Email of the user viewing this post. |
| `userId` | query | `string` | no | ID of the user viewing this post. |
| `language` | query | `string` | no | Retrieve the post translation in this language. |
| `traceableLinks` | query | `boolean` | no | Whether to include traceable links in the post. |
| `ignoreRequestDetails` | query | `boolean` | no | Ignore request details used for analytics. |
