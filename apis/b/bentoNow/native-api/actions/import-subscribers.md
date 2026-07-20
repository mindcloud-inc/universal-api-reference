# Import Subscribers with Bento Now

Imports subscribers into Bento Now without triggering automations.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batch/subscribers`
- **Base URL:** `https://app.bentonow.com/api`
- **Official documentation:** [Import Subscribers](https://bentonow.com/docs/subscribers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscribers[].email` | body | `string` | yes |
