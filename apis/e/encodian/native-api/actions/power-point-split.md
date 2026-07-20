# PowerPoint Split with Encodian

Splits a PowerPoint file in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PowerPoint/PowerPointSplit`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PowerPoint Split](https://support.encodian.com/hc/en-gb/articles/16517600430620)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | The Base64 encoded content of the Microsoft PowerPoint document. |
| `splitType` | body | `list` | yes | Select how to split the PowerPoint document. Accepted values: `0`, `1`, `2`. |
| `splitConfiguration` | body | `string` | no | Provide split configuration details. |
| `cultureName` | body | `string` | no | Culture name used when processing the request. |
