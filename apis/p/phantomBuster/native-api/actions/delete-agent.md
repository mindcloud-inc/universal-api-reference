# Delete Agent with PhantomBuster

Deletes an agent from PhantomBuster.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/delete`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Delete Agent](https://hub.phantombuster.com/reference/post_agents-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The PhantomBuster agent ID to delete. |
