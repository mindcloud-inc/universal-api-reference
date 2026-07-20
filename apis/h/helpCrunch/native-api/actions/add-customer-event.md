# Add Customer Event with HelpCrunch

Creates a new customer event in HelpCrunch.

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://api.helpcrunch.com/v1`
- **Official documentation:** [Add Customer Event](https://docs.helpcrunch.com/en/rest-api-v1/add-customer-event-v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer` | body | `number` | yes |
| `name` | body | `string` | yes |
