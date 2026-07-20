# Get Contact Mutation Request Status with Wooxy

Retrieves contact mutation request statuses from Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/request/find`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Get Contact Mutation Request Status](https://wooxy.com/api-documentation/contacts/get-add-update-remove-request-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Array of Wooxy contact mutation request IDs. |
