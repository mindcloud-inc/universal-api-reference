# Perform a Lookup enquiry for a mobile number with Routee

Creates a number lookup request in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/lookup`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Perform a Lookup enquiry for a mobile number](https://docs.routee.net/reference/perform-a-lookup-validation-for-a-mobile-nummer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | The mobile number that the service will use. Format with a '+' and country code e.g., +306948530920 (E.164 format). |
| `label` | body | `string` | no | A generic label which can be used for tagging the lookup HLR. |
