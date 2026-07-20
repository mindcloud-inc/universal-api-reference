# Rename Media with Sendible

## Endpoint

- **Method:** `PUT`
- **Path:** `0.2/tw/media`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Rename Media](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mediaId` | query | `string` | yes | The media ID to rename. |
| `name` | body | `string` | yes | New media name. |
