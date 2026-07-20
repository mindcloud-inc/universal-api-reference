# Add Subscribers To Groups By Email Address with SARE

Adds subscribers to SARE groups by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/group/add_emails`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Add Subscribers To Groups By Email Address](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Subscriber email addresses to add to the selected groups. |
| `groups[]` | body | `array<number>` | yes | Group identifiers that should receive the existing subscribers. |
