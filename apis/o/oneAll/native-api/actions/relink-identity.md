# Relink Identity with OneAll

Relinks a social identity to another user in OneAll.

## Endpoint

- **Method:** `PUT`
- **Path:** `/identities/<identity_token>/link.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Relink Identity](https://docs.oneall.com/api/resources/identities/relink-identity/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity_token` | path | `string` | yes | The OneAll identity token. |
