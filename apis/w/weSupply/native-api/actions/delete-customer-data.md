# Delete Customer Data with WeSupply

Deletes customer data from WeSupply.

## Endpoint

- **Method:** `POST`
- **Path:** `/gdpr/delete`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Delete Customer Data](https://documenter.getpostman.com/view/11859344/T17AiAYq#fa5b0e90-52c6-471d-8fa3-25fc906442d2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerEmail` | body | `string` | no | The customer email address whose data should be deleted. |
