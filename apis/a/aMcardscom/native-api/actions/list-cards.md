# List Cards with AMcards.com

Retrieves cards from your AMcards.com account.

## Endpoint

- **Method:** `GET`
- **Path:** `/card/`
- **Base URL:** `https://amcards.com/.api/v1`
- **Official documentation:** [List Cards](https://staging.amcards.com/docs/developers-only/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter cards by AMcards status code (`0` editable, `1` verifying address, `2` in the mail, `3` flagged, `4` delivered, `5` ready for print, `6` printed, `7` processing, `8` refunded/reported, `9` testing, `10` gift unavailable, `11` proof print, `12` return to sender). |
