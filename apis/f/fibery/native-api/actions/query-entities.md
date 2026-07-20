# Query Entities with Fibery

Retrieves entities from Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Query Entities](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Fibery Entity API query object. |
| `params` | body | `object` | no | Optional parameter values referenced from the query object. |
