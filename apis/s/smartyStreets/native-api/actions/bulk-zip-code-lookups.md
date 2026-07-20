# Bulk ZIP Code Lookups with Smarty-streets

Retrieves ZIP Code lookup details from Smarty-streets in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `https://us-zipcode.api.smarty.com/lookup`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Bulk ZIP Code Lookups](https://www.smarty.com/docs/apis/us-zipcode-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lookups[]` | body | `array<object>` | yes | Array of ZIP Code lookup objects. |
