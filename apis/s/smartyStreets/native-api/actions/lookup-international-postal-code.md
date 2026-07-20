# Lookup International Postal Code with Smarty-streets

Retrieves international postal code details from Smarty-streets by postal code.

## Endpoint

- **Method:** `GET`
- **Path:** `https://international-postal-code.api.smarty.com/lookup`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Lookup International Postal Code](https://www.smarty.com/docs/apis/international-postal-code-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Country name or ISO country code. |
| `postal_code` | query | `string` | yes | Postal code to look up. |
