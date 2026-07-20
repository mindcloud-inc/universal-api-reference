# Query Transactions with Sharetribe

Retrieves transactions from Sharetribe.

## Endpoint

- **Method:** `GET`
- **Path:** `transactions/query`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Query Transactions](https://www.sharetribe.com/api-reference/integration.html#query-transactions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdAtStart` | query | `date` | no | Filter transactions created on or after this ISO 8601 timestamp. |
| `createdAtEnd` | query | `date` | no | Filter transactions created before this ISO 8601 timestamp. |
| `userId` | query | `string` | no | Return transactions where this user is either the customer or provider. |
| `customerId` | query | `string` | no | Return only transactions where this user is the customer. |
| `providerId` | query | `string` | no | Return only transactions where this user is the provider. |
| `listingId` | query | `string` | no | Return only transactions for this listing. |
| `lastTransitions` | query | `string` | no | Comma-separated list of last transition names to match. Send multiple values as a string separated by `,`. |
| `processNames` | query | `string` | no | Comma-separated list of transaction process names to match. Send multiple values as a string separated by `,`. |
| `states` | query | `string` | no | Comma-separated list of transaction states to match. Send multiple values as a string separated by `,`. |
| `hasBooking` | query | `boolean` | no | Filter by whether a booking is present. |
| `hasStockReservation` | query | `boolean` | no | Filter by whether a stock reservation is present. |
| `hasPayin` | query | `boolean` | no | Filter by whether the transaction has at least one pay-in. |
| `hasMessage` | query | `boolean` | no | Filter by whether the transaction has at least one message. |
| `bookingStates` | query | `string` | no | Comma-separated list of booking states to match. Send multiple values as a string separated by `,`. |
| `stockReservationStates` | query | `string` | no | Comma-separated list of stock reservation states to match. Send multiple values as a string separated by `,`. |
| `bookingStart` | query | `string` | no | Booking start range using START,END, START,, or ,END with ISO 8601 timestamps. |
| `bookingEnd` | query | `string` | no | Booking end range using START,END, START,, or ,END with ISO 8601 timestamps. |
