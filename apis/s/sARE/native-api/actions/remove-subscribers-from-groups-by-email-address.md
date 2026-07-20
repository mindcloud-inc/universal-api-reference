# Remove Subscribers From Groups By Email Address with SARE

Removes subscribers from SARE groups by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/group/remove_emails`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Remove Subscribers From Groups By Email Address](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Subscriber email addresses to remove from the selected groups. |
| `groups[]` | body | `array<number>` | yes | Group identifiers that should lose the existing subscribers. |
