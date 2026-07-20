# Get Prospect Verification Status with Saleshandy

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects/verification-status`
- **Base URL:** `https://open-api.saleshandy.com/v1`
- **Official documentation:** [Get Prospect Verification Status](https://developer.saleshandy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Email addresses to look up verification status for. |
