# Get Account Invoice with Tarvent

Retrieves an account invoice from Tarvent by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.tarvent.com`
- **Official documentation:** [Get Account Invoice](https://developer.tarvent.com/queries/accountInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The Tarvent invoice ID to fetch. |
