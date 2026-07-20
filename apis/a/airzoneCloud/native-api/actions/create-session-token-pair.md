# Create Session Token Pair with Airzone Cloud

Creates a session token pair in Airzone Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/auth/login`
- **Base URL:** `https://m.airzonecloud.com/api/v1`
- **Official documentation:** [Create Session Token Pair](https://developers.airzonecloud.com/docs/web-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Airzone Cloud account email used to create a session token pair. |
| `password` | body | `string` | yes | Airzone Cloud account password used to create a session token pair. |
