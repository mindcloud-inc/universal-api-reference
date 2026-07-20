# Autocomplete with People Data Labs

## Endpoint

- **Method:** `GET`
- **Path:** `/autocomplete`
- **Base URL:** `https://api.peopledatalabs.com/v5`
- **Official documentation:** [Autocomplete](https://docs.peopledatalabs.com/docs/reference-autocomplete-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field` | query | `string` | yes | Autocomplete field value such as company, title, school, skill, location_name, industry, or website. |
| `text` | query | `string` | no | Starting text used as the seed for autocompletion. |
