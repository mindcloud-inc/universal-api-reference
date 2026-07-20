# Upsert Event Discounts with Universe

Creates or updates discounts for a Universe event.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [Upsert Event Discounts](https://developers.universe.com/docs/what-data-is-available)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query or mutation document to execute. The default is an event discounts upsert mutation for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables as a JSON object string for the default discount upsert mutation. |
