# Retrieve information for a specific email address from a specific campaign with Routee

Retrieves information for a specific email address from a specific campaign in Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:id/email/:email`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve information for a specific email address from a specific campaign](https://docs.routee.net/reference/retrieving-information-for-a-specific-email-address-from-a-specific-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Campaign id |
| `email` | path | `string` | yes | Email address to retrieve the information |
