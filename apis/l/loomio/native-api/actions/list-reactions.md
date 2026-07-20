# List Reactions with Loomio

Retrieves reactions from Loomio.

## Endpoint

- **Method:** `GET`
- **Path:** `/reactions`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [List Reactions](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/reactions_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `discussion_id` | query | `string` | no | The Loomio discussion ID to list reactions for. |
