# Add Carrier with Shipday

Creates a new carrier in Shipday.

## Endpoint

- **Method:** `POST`
- **Path:** `/carriers`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Add Carrier](https://docs.shipday.com/reference/add-a-carrier-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Full name of the carrier. |
| `email` | body | `string` | no | Email address for the carrier. |
| `phoneNumber` | body | `string` | no | Phone number for the carrier. |
