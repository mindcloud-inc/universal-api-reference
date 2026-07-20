# Delete Webhook By URL with Loop & Tie

Deletes a webhook from Loop & Tie by URL.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/teams/:teamId/hooks`
- **Base URL:** `https://api.loopandtie.com/v1`
- **Official documentation:** [Delete Webhook By URL](https://docs.loopandtie.com/reference/teamsteam_idhooks-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hook[url]` | query | `string` | no | Webhook URL to remove. |
| `teamId` | path | `string` | no | The Loop & Tie team ID. |
