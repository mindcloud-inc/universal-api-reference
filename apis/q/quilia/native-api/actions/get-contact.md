# Get Contact with Quilia

## Endpoint

- **Method:** `GET`
- **Path:** `contacts/:id`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [Get Contact](https://api.quilia.dev/v2#tag/contacts/GET/contacts/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the contact to retrieve |
| `type` | query | `list<string>` | yes | The type of contact to retrieve Accepted values: `company`, `people`. |
