# Detect Disposable Email with Minelead

Checks whether an email address is disposable in Minelead.

## Endpoint

- **Method:** `GET`
- **Path:** `/detect-disposable`
- **Base URL:** `https://api.minelead.io/v1`
- **Official documentation:** [Detect Disposable Email](https://api.minelead.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to inspect for disposability. |
