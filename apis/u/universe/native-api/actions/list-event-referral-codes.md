# List Event Referral Codes with Universe

Retrieves referral codes for a specific Universe event.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [List Event Referral Codes](https://developers.universe.com/docs/what-data-is-available)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query document to execute for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables object for the referral codes query. |
