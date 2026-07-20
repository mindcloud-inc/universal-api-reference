# List Addresses with GetResponse

Retrieves a list of addresses from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/addresses`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [List Addresses](https://apireference.getresponse.com/#operation/getAddressList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[name]` | query | `string` | no | Filter addresses by name |
| `query[firstName]` | query | `string` | no | Filter addresses by first name |
| `query[lastName]` | query | `string` | no | Filter addresses by last name |
| `query[address1]` | query | `string` | no | Filter by address line 1 |
| `query[address2]` | query | `string` | no | Filter by address line 2 |
| `query[city]` | query | `string` | no | Filter addresses by city |
| `query[zip]` | query | `string` | no | Filter addresses by ZIP code |
| `query[province]` | query | `string` | no | Filter addresses by province |
| `query[provinceCode]` | query | `string` | no | Filter addresses by province code |
| `query[phone]` | query | `string` | no | Filter addresses by phone |
| `query[company]` | query | `string` | no | Filter addresses by company |
| `query[createdOn][from]` | query | `string` | no | Return addresses created on or after this date |
| `query[createdOn][to]` | query | `string` | no | Return addresses created on or before this date |
| `sort[createdOn]` | query | `string` | no | Sort addresses by creation date |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
