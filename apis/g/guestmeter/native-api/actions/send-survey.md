# Send Survey with Guestmeter

Creates a guest survey request in Guestmeter.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendSurvey`
- **Base URL:** `https://www.guestmeter.com/api`
- **Official documentation:** [Send Survey](https://www.guestmeter.com/docs/api#add-guest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkoutDate` | query | `string` | no | Optional send date in DD.MM.YYYY or DD-MM-YYYY format. |
| `guestEmail` | query | `string` | yes | Guest email address. |
| `guestName` | query | `string` | yes | Guest full name. |
| `guestPhone` | query | `string` | no | Guest mobile number in international format. |
| `integrationID` | query | `string` | no | Reference ID for the guest in your source system (for example reservation ID). |
| `languageCode` | query | `string` | no | Two-letter language code (for example en). |
| `primarySendMethod` | query | `string` | no | Preferred channel when both email and phone exist: email or sms. |
| `roomNumber` | query | `string` | no | Guest room number or table number. |
