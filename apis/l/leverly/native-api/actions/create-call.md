# Create Call with Leverly

## Endpoint

- **Method:** `POST`
- **Path:** `/ingestor/process`
- **Base URL:** `https://app.leverly.com/main`
- **Official documentation:** [Create Call](https://leverly.com/kb/http-posting/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address1` | body | `string` | no | Lead's address. |
| `area` | body | `string` | no | Lead's area of interest. |
| `callDelay` | body | `number` | no | Delay before the initial call in seconds. |
| `callerId` | body | `string` | no | Caller ID to display on leg 1 of the call. |
| `city` | body | `string` | no | Lead's city. |
| `comments` | body | `string` | no | Lead comments. |
| `companyName` | body | `string` | no | Lead's company name. |
| `email` | body | `string` | no | Lead's email address. |
| `keyword` | body | `string` | no | Lead's keyword. |
| `lastName` | body | `string` | no | Lead's last name. |
| `leadSource` | body | `string` | no | Lead's source. |
| `location` | body | `string` | no | Lead's location. |
| `Phone2` | body | `string` | no | Lead's second phone number. |
| `Phone3` | body | `string` | no | Lead's third phone number. |
| `Phone4` | body | `string` | no | Lead's fourth phone number. |
| `program` | body | `string` | no | Lead's program of interest. |
| `repPhone` | body | `string` | no | Representative phone number. Separate multiple numbers with commas. |
| `routingType` | body | `number` | no | 1 = Step ringing, 2 = Round robin, 3 = Simultaneous. |
| `state` | body | `string` | no | Lead's state. |
| `vendorLeadID` | body | `string` | no | Vendor lead identifier used to reconcile and stop a submitted call later. |
| `zip` | body | `string` | no | Lead's ZIP code. |
| `firstName` | body | `string` | yes | Lead's first name. |
| `Phone1` | body | `string` | yes | Lead's primary phone number. |
