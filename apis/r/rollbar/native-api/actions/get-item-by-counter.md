# Get Item By Counter with Rollbar

Retrieves an item from Rollbar by project counter.

## Endpoint

- **Method:** `GET`
- **Path:** `/item_by_counter/:counter`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get Item By Counter](https://docs.rollbar.com/reference/get-an-item-by-project-counter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `counter` | path | `number` | yes | Project counter for the item. |
