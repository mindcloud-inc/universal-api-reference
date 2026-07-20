# Update Airmeet Status with Airmeet

Updates the status of an Airmeet event.

## Endpoint

- **Method:** `POST`
- **Path:** `/airmeet/{airmeetId}/status`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [Update Airmeet Status](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `status` | body | `string` | yes | Target Airmeet status such as ONGOING, PAUSED, FINISHED, or ARCHIVE. |
