# Add Speaker with Airmeet

Creates a new speaker in Airmeet.

## Endpoint

- **Method:** `POST`
- **Path:** `/airmeet/{airmeetId}/speaker`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [Add Speaker](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `email` | body | `string` | yes | Speaker email address. |
| `name` | body | `string` | yes | Speaker name. |
