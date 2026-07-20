# Retrieve Contact by Cookie Token with Polaria

Retrieves a contact from Polaria by cookie token.

## Endpoint

- **Method:** `GET`
- **Path:** `/widgets/[:api_key]/contacts/retrieve`
- **Base URL:** `https://app.polaria.ai/rest/v2`
- **Official documentation:** [Retrieve Contact by Cookie Token](https://help.polaria.ai/hc/rest-api-contacts/get-widgets-api_key-contacts-retrieve-retrieve-a-contact-by-cookie_token?lang=en)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `api_key` | path | `string` | yes |
| `cookie_token` | query | `string` | yes |
