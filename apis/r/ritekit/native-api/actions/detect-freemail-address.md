# Detect Freemail Address with Ritekit

Detects whether an email uses a freemail provider.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/person-insights/freemail-detection`
- **Base URL:** `https://api.ritekit.com`
- **Official documentation:** [Detect Freemail Address](https://documenter.getpostman.com/view/2010712/SzS7Qku5?version=latest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain or email value to check for freemail detection. |
