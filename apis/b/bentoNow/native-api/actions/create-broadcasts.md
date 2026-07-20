# Create Broadcasts with Bento Now

Creates a broadcast campaign in Bento Now.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batch/broadcasts`
- **Base URL:** `https://app.bentonow.com/api`
- **Official documentation:** [Create Broadcasts](https://bentonow.com/docs/broadcasts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `broadcasts[].content` | body | `string` | yes |
| `broadcasts[].name` | body | `string` | yes |
| `broadcasts[].subject` | body | `string` | yes |
| `broadcasts[].type` | body | `string` | yes |
