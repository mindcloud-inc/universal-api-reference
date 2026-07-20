# Create Contact with SMSEdge

Creates a new contact in a SMSEdge list.

## Endpoint

- **Method:** `POST`
- **Path:** `/numbers/create/`
- **Base URL:** `https://api.smsedge.com/v1`
- **Official documentation:** [Create Contact](https://developers.smsedge.io/reference/numbers-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `birthday` | query | `string` | no | Birthday in year-month-day format |
| `country` | query | `string` | no | Country ISO or name for localized formatting |
| `country_id` | query | `number` | no | ID of country when the phone number is local format |
| `email` | query | `string` | no | E-mail of recipient |
| `gender` | query | `string` | no | Recipient gender using the provider's accepted values |
| `list_id` | query | `number` | yes | Number will be added to list with this ID |
| `lname` | query | `string` | no | Last name of recipient |
| `name` | query | `string` | no | Name of recipient |
| `number` | query | `string` | yes | Phone number of recipient |
