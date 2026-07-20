# Synchronize Identity with OneAll

Synchronizes a social identity with its network in OneAll.

## Endpoint

- **Method:** `PUT`
- **Path:** `/identities/<identity_token>/synchronize.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Synchronize Identity](https://docs.oneall.com/api/resources/identities/synchronize-identity/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity_token` | path | `string` | yes | The OneAll identity token. |
