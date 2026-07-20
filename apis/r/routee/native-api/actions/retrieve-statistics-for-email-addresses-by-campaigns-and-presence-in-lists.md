# Retrieve statistics for email addresses by campaigns and presence in lists with Routee

Retrieves statistics for email addresses by campaigns and presence in lists from Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/campaigns`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve statistics for email addresses by campaigns and presence in lists](https://docs.routee.net/reference/retrieving-statistics-for-email-addresses-by-campaigns-and-presence-in-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | no | array of contacts ["example@yourdomain.com", "example2@yourdomain.com"] |
