# Suggest International Addresses with Smarty-streets

Finds international address suggestions in Smarty-streets by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `https://international-autocomplete.api.smarty.com/v2/lookup`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Suggest International Addresses](https://www.smarty.com/docs/apis/international-autocomplete-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | ISO3 country code for the desired address. |
| `search` | query | `string` | yes | Address text typed so far. |
