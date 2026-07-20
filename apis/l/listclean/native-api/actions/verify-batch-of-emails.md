# Verify Batch Of Emails with Listclean

Verifies up to 3,000 email addresses in Listclean.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/email/batch`
- **Base URL:** `https://api.listclean.xyz/v1`
- **Official documentation:** [Verify Batch Of Emails](https://api.listclean.xyz/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Email addresses to verify. The Listclean API accepts up to 3000 emails. |
