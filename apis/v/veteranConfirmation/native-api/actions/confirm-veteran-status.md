# Confirm Veteran Status with Veteran Confirmation

## Endpoint

- **Method:** `POST`
- **Path:** `/status`
- **Base URL:** `https://sandbox-api.va.gov/services/veteran-confirmation/v1`
- **Official documentation:** [Confirm Veteran Status](https://developer.va.gov/explore/api/veteran-confirmation/docs?version=current)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | yes | Person's first name. |
| `middleName` | body | `string` | no | Person's middle name. |
| `lastName` | body | `string` | yes | Person's last name. |
| `birthDate` | body | `date` | yes | Birth date in YYYY-MM-DD format. |
| `gender` | body | `string` | no | Gender value; only M or F helps the search currently. |
| `streetAddressLine1` | body | `string` | yes | Current residence street address line 1. |
| `streetAddressLine2` | body | `string` | no | Current residence street address line 2. |
| `streetAddressLine3` | body | `string` | no | Current residence street address line 3. |
| `city` | body | `string` | yes | Current residence city. |
| `state` | body | `string` | yes | Current residence state. |
| `zipCode` | body | `string` | yes | Current residence zip code. |
| `country` | body | `string` | yes | Current residence country. |
| `homePhoneNumber` | body | `string` | no | Home phone number. |
| `mothersMaidenName` | body | `string` | no | Mother's maiden name. |
| `birthPlaceCity` | body | `string` | no | Birth place city. |
| `birthPlaceState` | body | `string` | no | Birth place state. |
| `birthPlaceCountry` | body | `string` | no | Birth place country. |
