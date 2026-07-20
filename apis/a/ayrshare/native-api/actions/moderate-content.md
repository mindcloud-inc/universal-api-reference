# Moderate Content with Ayrshare

Checks text for harmful or inappropriate content in Ayrshare.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/moderation`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Moderate Content](https://www.ayrshare.com/docs/apis/validate/moderation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to submit for moderation. |
