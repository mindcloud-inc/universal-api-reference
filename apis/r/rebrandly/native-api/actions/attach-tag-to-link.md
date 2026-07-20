# Attach Tag To Link with Rebrandly

Attaches a tag to a link in Rebrandly.

## Endpoint

- **Method:** `POST`
- **Path:** `/links/:lid/tags/:tid`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Attach Tag To Link](https://developers.rebrandly.com/docs/attaching-a-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lid` | path | `string` | yes | Unique identifier of the link to update. |
| `tid` | path | `string` | yes | Unique identifier of the tag to attach. |
