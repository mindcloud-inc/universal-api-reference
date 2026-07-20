# Suggest US Addresses with Smarty-streets

Finds US address suggestions in Smarty-streets by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `https://us-autocomplete-pro.api.smarty.com/lookup`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Suggest US Addresses](https://www.smarty.com/docs/apis/us-autocomplete-pro-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Address text typed so far. |
