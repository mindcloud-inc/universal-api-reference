# Create SRT Transformer with Stripo

Creates an SRT transformer in Stripo.

## Endpoint

- **Method:** `POST`
- **Path:** `/srt`
- **Base URL:** `https://my.stripo.email/emailgeneration/v1`
- **Official documentation:** [Create SRT Transformer](https://api.stripo.email/reference/savesrtconfig)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `config` | body | `object` | yes | Transformer configuration body. |
| `name` | body | `string` | yes | SRT rule name. |
