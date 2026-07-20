# Delete Subscriber with Laposta

Deletes an existing subscriber from Laposta.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/member/:memberId`
- **Base URL:** `https://api.laposta.nl/v2`
- **Official documentation:** [Delete Subscriber](https://api.laposta.nl/doc/index.en.php#members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberId` | path | `string` | yes | The subscriber ID or email address to delete. |
| `list_id` | query | `string` | yes | The ID of the list that owns the subscriber. |
