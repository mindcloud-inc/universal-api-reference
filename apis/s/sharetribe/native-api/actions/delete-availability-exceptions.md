# Delete Availability Exceptions with Sharetribe

Deletes existing availability exceptions from Sharetribe.

## Endpoint

- **Method:** `POST`
- **Path:** `availability_exceptions/delete`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Delete Availability Exceptions](https://www.sharetribe.com/api-reference/integration.html#delete-availability-exceptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The ID of the availability exception to delete. |
