# Domain Status with Tomba

Retrieves the status of a domain in Tomba.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain-status`
- **Base URL:** `https://api.tomba.io/v1`
- **Official documentation:** [Domain Status](https://docs.tomba.io/api/~endpoints#domain-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain to classify as webmail or disposable. |
