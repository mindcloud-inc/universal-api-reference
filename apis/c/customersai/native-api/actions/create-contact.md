# Create Contact with Customers.ai

Creates an SMS contact in Customers.ai, or updates an existing match.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.mobilemonkey.com/public`
- **Official documentation:** [Create Contact](https://customers.ai/help/l/en/category/doq3ewxla3-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PHONE` | body | `string` | yes | Phone number in E.123 international notation. US and Canadian numbers only. |
| `first_name` | body | `string` | no | First name. |
| `last_name` | body | `string` | no | Last name. |
| `EMAIL` | body | `string` | no | Email address stored as the EMAIL attribute. |
