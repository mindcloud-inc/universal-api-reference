# Retrieve information for specific email address from a mailing list with Routee

Retrieves information for specific email address from a mailing list in Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/addressbooks/:id/emails/:email`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve information for specific email address from a mailing list](https://docs.routee.net/reference/retrieving-information-for-specific-email-address-from-a-mailing-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | List ID |
| `email` | path | `string` | yes | Email address information is desired on |
