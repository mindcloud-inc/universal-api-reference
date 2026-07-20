# Delete Flight Alert Listener with Airlabs

Deletes a flight alert listener from Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/unlisten`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [Delete Flight Alert Listener](https://airlabs.co/docs/alert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listener_id` | query | `number` | yes | ID of the previously created listener to delete. |
