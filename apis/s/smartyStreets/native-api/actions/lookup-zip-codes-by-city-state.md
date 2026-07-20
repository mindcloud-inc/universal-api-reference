# Lookup ZIP Codes By City State with Smarty-streets

Finds ZIP Codes in Smarty-streets by city and state.

## Endpoint

- **Method:** `GET`
- **Path:** `https://us-zipcode.api.smarty.com/lookup`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Lookup ZIP Codes By City State](https://www.smarty.com/docs/apis/us-zipcode-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | query | `string` | yes | City name to look up. |
| `state` | query | `string` | yes | State name or two-letter abbreviation. |
