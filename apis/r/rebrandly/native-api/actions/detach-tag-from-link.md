# Detach Tag From Link with Rebrandly

Detaches a tag from a link in Rebrandly.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/links/:lid/tags/:tid`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Detach Tag From Link](https://developers.rebrandly.com/docs/detaching-a-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lid` | path | `string` | yes | Unique identifier of the link to update. |
| `tid` | path | `string` | yes | Unique identifier of the tag to detach. |
