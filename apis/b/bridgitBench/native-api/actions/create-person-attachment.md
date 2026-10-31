# Create Person Attachment with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/attachments`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Person Attachment](https://developers.gobridgit.com/reference/personattachments_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID |
| `personId` | path | `number` | yes | The person ID |
| `name` | body | `string` | yes | — |
| `isPrivate` | body | `boolean` | yes | — |
