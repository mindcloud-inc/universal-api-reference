# Lookup Phone Operator with JetAPI

Finds a phone operator in JetAPI by number.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/operators/search`
- **Base URL:** `https://api.jetapi.io`
- **Official documentation:** [Lookup Phone Operator](https://docs.jetapi.io/#c22bc81c-94fe-4a10-b48e-6b6d5ef3089b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | query | `string` | yes | Phone number in international format. Special characters are allowed. |
