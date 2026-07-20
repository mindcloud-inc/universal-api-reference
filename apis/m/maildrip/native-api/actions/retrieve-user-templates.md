# Retrieve User Templates with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/template`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Retrieve User Templates](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Template type ["web-builder" \| "speditor"] - when it's not passed in, strippo templates are returned by default |
