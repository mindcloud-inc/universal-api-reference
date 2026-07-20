# Create Webhook with Fluxguard

Creates a new webhook in Fluxguard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/account/webhook`
- **Base URL:** `https://api.fluxguard.com`
- **Official documentation:** [Create Webhook](https://fluxguard.com/how-to-guides/use-our-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook destination URL. |
