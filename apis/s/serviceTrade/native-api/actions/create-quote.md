# Create Quote with ServiceTrade

Creates a new quote in ServiceTrade.

## Endpoint

- **Method:** `POST`
- **Path:** `quote`
- **Base URL:** `https://api.servicetrade.com/api`
- **Official documentation:** [Create Quote](https://api.servicetrade.com/api/docs#resource-quote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vendorId` | body | `number` | yes | Vendor company performing the quoted work. |
| `locationId` | body | `number` | yes | Location where the quote applies. |
| `name` | body | `string` | yes | Name of the quote. |
| `description` | body | `string` | yes | Description of the work to be quoted. |
| `jobType` | body | `string` | yes | Job type the quote should generate. |
| `serviceRequestIds` | body | `list<number>` | yes | Service requests fulfilled by the quote. Send multiple values as a array. |
