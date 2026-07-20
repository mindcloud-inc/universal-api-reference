# Create Availability Exceptions with Sharetribe

Creates new availability exceptions in Sharetribe.

## Endpoint

- **Method:** `POST`
- **Path:** `availability_exceptions/create`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Create Availability Exceptions](https://www.sharetribe.com/api-reference/integration.html#create-availability-exceptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listingId` | body | `string` | yes | The listing ID. |
| `start` | body | `date` | yes | Availability exception interval start time in ISO 8601 format. |
| `end` | body | `date` | yes | Availability exception interval end time in ISO 8601 format. |
| `seats` | body | `number` | yes | Number of available seats for the given range. Set to 0 to block the range. |
