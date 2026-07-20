# Lookup Phone Number with Sendblue

Determines whether a phone number supports iMessage or SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/evaluate-service`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Lookup Phone Number](https://docs.sendblue.com/api/resources/lookups/methods/lookup_number/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | The number to evaluate in E.164 format. |
