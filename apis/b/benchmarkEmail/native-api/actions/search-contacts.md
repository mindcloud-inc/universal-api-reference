# Search Contacts with Benchmark Email

Finds contacts in Benchmark Email by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/Contact/ContactDetails`
- **Base URL:** `https://clientapi.benchmarkemail.com`
- **Official documentation:** [Search Contacts](https://developer.benchmarkemail.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Search` | query | `string` | yes | Email address to search for. |
| `SearchFilter` | query | `string` | no | Optional search filter. |
