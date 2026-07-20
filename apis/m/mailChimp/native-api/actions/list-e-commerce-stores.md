# List E-commerce Stores with Mailchimp

Retrieves e-commerce stores from Mailchimp.

## Endpoint

- **Method:** `GET`
- **Path:** `ecommerce/stores`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [List E-commerce Stores](https://mailchimp.com/developer/marketing/api/ecommerce-stores/list-stores/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | A comma-separated list of fields to return. Send multiple values as a array. |
| `exclude_fields` | query | `string` | no | A comma-separated list of fields to exclude from the returned response. |
