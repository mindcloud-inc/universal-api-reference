# Create Booth with Airmeet

Creates a new booth in Airmeet.

## Endpoint

- **Method:** `POST`
- **Path:** `/airmeet/{airmeetId}/booths`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [Create Booth](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `name` | body | `string` | yes | Title for the booth. |
