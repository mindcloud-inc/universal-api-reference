# Verify Email (POST) with Email Verifier Api

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/`
- **Base URL:** `https://emailverifierapi.com`
- **Official documentation:** [Verify Email (POST)](https://emailverifierapi.com/api-docs/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to verify. |
