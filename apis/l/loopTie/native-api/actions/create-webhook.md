# Create Webhook with Loop & Tie

Creates a new webhook in Loop & Tie.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:teamId/hooks`
- **Base URL:** `https://api.loopandtie.com/v1`
- **Official documentation:** [Create Webhook](https://docs.loopandtie.com/reference/teamsteam_idhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hook[url]` | query | `string` | no | Public HTTPS endpoint to receive Loop & Tie webhook events. |
| `teamId` | path | `string` | no | The Loop & Tie team ID. |
