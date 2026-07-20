# Create Prospect with ManyReach

Creates a new prospect in ManyReach.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.manyreach.com/api/v2/prospects`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Create Prospect](https://api.manyreach.com/api#v2/tag/prospect)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseListId` | body | `string` | yes | List ID to attach the prospect to. |
| `email` | body | `string` | yes | Prospect email address. |
