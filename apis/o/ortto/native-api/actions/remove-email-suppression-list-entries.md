# Remove Email Suppression List Entries with Ortto

## Endpoint

- **Method:** `PUT`
- **Path:** `/suppression-list/email/remove`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Remove Email Suppression List Entries](https://help.ortto.com/a-836-managing-the-email-suppression-list-via-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Email addresses to remove from the suppression list. |
