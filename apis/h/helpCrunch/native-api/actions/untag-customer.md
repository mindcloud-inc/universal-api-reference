# Untag Customer with HelpCrunch

Removes tags from a customer in HelpCrunch.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/customers/:customerId/tags`
- **Base URL:** `https://api.helpcrunch.com/v1`
- **Official documentation:** [Untag Customer](https://docs.helpcrunch.com/en/rest-api-v1/untag-customer-v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `tags` | body | `list<string>` | yes |
