# Resend Order with Mighty Tix

Resends an order in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Resend Order](https://mightytix.com/docs/admin-api#mutation-resendOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | Order ID from the Mighty Tix Admin GraphQL docs. |
