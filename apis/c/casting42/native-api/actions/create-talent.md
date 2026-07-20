# Create Talent with Casting42

Creates a new talent in Casting42.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/talents`
- **Base URL:** `https://casting42.com`
- **Official documentation:** [Create Talent](https://documenter.getpostman.com/view/24607394/2s9YR6buRP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | yes | First name of the talent. |
| `lastName` | body | `string` | yes | Last name of the talent. |
| `email` | body | `string` | no | Email address of the talent. |
