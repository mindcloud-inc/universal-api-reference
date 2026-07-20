# Complete Upload with Sendible

## Endpoint

- **Method:** `PUT`
- **Path:** `0.2/tw/uploads`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Complete Upload](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Upload intent ID to complete. |
| `uploadedParts` | body | `list<object>` | yes | Completed upload parts with eTag and partNumber entries. |
