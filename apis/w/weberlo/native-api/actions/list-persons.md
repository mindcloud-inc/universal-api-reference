# List Persons with Weberlo

Retrieves a list of persons from Weberlo.

## Endpoint

- **Method:** `POST`
- **Path:** `/person/list`
- **Base URL:** `https://connect.weberlo.com`
- **Official documentation:** [List Persons](https://developers.weberlo.com/#tag/Person/paths/~1person~1list/post)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | body | `string` | yes | Start of the person search window. |
| `end_date` | body | `string` | yes | End of the person search window. |
| `type` | body | `string` | yes | Person type, for example lead. |
| `email` | query | `string` | no | Filter by email. |
| `first_name` | query | `string` | no | Filter by first name. |
| `last_name` | query | `string` | no | Filter by last name. |
| `name` | query | `string` | no | Filter by full name. |
| `phone` | query | `string` | no | Filter by phone. |
| `country_code` | query | `string` | no | Filter by country code. |
