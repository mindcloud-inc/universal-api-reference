# Verify Email with EndBounce

Creates an email verification result in EndBounce.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/verify`
- **Base URL:** `https://api.endbounce.com/api/integrations`
- **Official documentation:** [Verify Email](https://app.endbounce.com/integrations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to verify. |
