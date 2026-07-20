# Delete SMS with Seven

Deletes an SMS from Seven.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sms`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Delete SMS](https://docs.seven.io/en/rest-api/endpoints/sms#delete-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | A list of the SMS to be deleted. Enter the respective &#x27;id&#x27;s of the SMS to be deleted here. |
