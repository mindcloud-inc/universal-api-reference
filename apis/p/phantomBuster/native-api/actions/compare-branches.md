# Compare Branches with PhantomBuster

Retrieves differences between branches in PhantomBuster.

## Endpoint

- **Method:** `GET`
- **Path:** `/branches/diff`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Compare Branches](https://hub.phantombuster.com/reference/get_branches-diff)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Name of the script branch to fetch the diff from. |
