# Get Network Member by Email with Mighty Networks

Finds a network member in Mighty Networks by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/members/by_email`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Get Network Member by Email](https://docs.mightynetworks.com/api-reference/members/return-a-single-member-by-email-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `email` | query | `string` | yes | Email address of the member. |
