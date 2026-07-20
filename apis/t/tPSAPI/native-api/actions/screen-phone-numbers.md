# Screen Phone Numbers with TPS API

Screens phone numbers against TPS and CTPS lists in TPS API.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://service.tpsapi.com`
- **Official documentation:** [Screen Phone Numbers](https://tpsapi.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone_numbers` | body | `list<string>` | yes | Phone numbers to screen against the selected TPS lists. |
| `checkTps` | body | `boolean` | no | Screen numbers against the TPS list. |
| `checkCtps` | body | `boolean` | no | Screen numbers against the CTPS list. |
| `returnCallableNumbersOnly` | body | `boolean` | no | Return only numbers that are not on the selected list or lists. |
| `returnPrettierNumbers` | body | `boolean` | no | Include a prettier phone number field in the response. |
| `returnDateAdded` | body | `boolean` | no | Include the date each number was added to the selected list or lists. |
| `noLogging` | body | `boolean` | no | Prevent the provider from storing full numbers in logs. |
