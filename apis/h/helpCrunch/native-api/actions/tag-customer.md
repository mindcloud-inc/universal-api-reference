# Tag Customer with HelpCrunch

Adds tags to a customer in HelpCrunch.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/:customerId/tags`
- **Base URL:** `https://api.helpcrunch.com/v1`
- **Official documentation:** [Tag Customer](https://docs.helpcrunch.com/en/rest-api-v1/tag-customer-v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `tags` | body | `list<string>` | yes |
