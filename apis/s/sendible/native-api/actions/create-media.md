# Create Media with Sendible

## Endpoint

- **Method:** `POST`
- **Path:** `0.2/tw/media`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Create Media](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `components.original` | body | `string` | yes | Upload intent ID for the original media component. |
| `name` | body | `string` | yes | Media name. |
