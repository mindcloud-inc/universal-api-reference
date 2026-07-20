# Validate US Addresses In Bulk with Smarty-streets

Retrieves validated US addresses from Smarty-streets in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `https://us-street.api.smarty.com/street-address`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Validate US Addresses In Bulk](https://www.smarty.com/docs/apis/us-street-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addresses[]` | body | `array<object>` | yes | Array of US address lookup objects. |
