# List Calls by Participant Email with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [List Calls by Participant Email](https://docs.buildbetter.ai/pages/api/graphql-queries#filtering)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the participant to match on the call attendees. |
| `limit` | body | `number` | no | Maximum number of calls to return. |
