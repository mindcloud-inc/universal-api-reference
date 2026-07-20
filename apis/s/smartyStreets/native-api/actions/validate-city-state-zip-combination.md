# Validate City State ZIP Combination with Smarty-streets

Retrieves validation details for a city, state, and ZIP combination in Smarty-streets.

## Endpoint

- **Method:** `GET`
- **Path:** `https://us-zipcode.api.smarty.com/lookup`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Validate City State ZIP Combination](https://www.smarty.com/docs/apis/us-zipcode-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | query | `string` | yes | City name to validate. |
| `state` | query | `string` | yes | State name or two-letter abbreviation. |
| `zipcode` | query | `string` | yes | ZIP Code to validate with the city and state. |
