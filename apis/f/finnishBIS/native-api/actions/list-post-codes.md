# List Post Codes with Finnish BIS

Retrieves postal code details from Finnish BIS.

## Endpoint

- **Method:** `GET`
- **Path:** `/post_codes`
- **Base URL:** `https://avoindata.prh.fi/opendata-ytj-api/v3`
- **Official documentation:** [List Post Codes](https://avoindata.prh.fi/opendata-ytj-api/v3/schema?lang=en)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lang` | query | `list<string>` | yes | Language code for postal code details. Accepted values: `en`, `fi`, `sv`. |
