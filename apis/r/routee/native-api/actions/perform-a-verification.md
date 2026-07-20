# Perform a verification with Routee

Creates a new verification in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/2step`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Perform a verification](https://docs.routee.net/reference/verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `method` | body | `string` | yes | The method which will be used to send the 2step verification. Values: "sms", "voice". |
| `type` | body | `string` | yes | The type of the message. Value: "code". |
| `recipient` | body | `string` | yes | The recipient that will receive the 2step verification. For sms method format with a '+' and country code e.g., +306948530920 (E.164 format). |
| `template` | body | `string` | yes | The template of the message. It must contain a @@pin that will be replaced by the generated code. |
| `arguments` | body | `string` | no | If the template is for example '@@name your code is @@pin' and the argument has a property name: 'Nick' the message will be 'Nick your code is 4232'. Note that if the template contains a @@ placeholder and a value is not present in the arguments property it will stay as is. |
| `templateCountry` | body | `string` | no | Country in [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements) alpha 2 format (GR, US etc.). The country to use in order to select a translated template (if defined in Routee web interface) |
| `originator` | body | `string` | no | The senderId that will be set when sending the SMS |
| `lifetimeInSeconds` | body | `number` | no | How many seconds this verification will remain active. After that time passes the verification status will be Expired. |
| `maxRetries` | body | `number` | no | Defines the number of times the user can re-confirm the verification before the verification changes its state to Failed. |
| `digits` | body | `number` | no | The number of digits of the generated random numeric code. |
| `restrictions` | body | `object` | no | [OPTIONAL] Provide the registered Content Template ID and Principal Entity ID to ensure the message is not rejected by TRAI regulations. |
