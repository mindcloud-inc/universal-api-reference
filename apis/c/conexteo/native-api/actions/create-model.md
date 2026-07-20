# Create Model with Conexteo

Creates a message template in Conexteo.

## Endpoint

- **Method:** `POST`
- **Path:** `/models`
- **Base URL:** `https://api.conexteo.com`
- **Official documentation:** [Create Model](https://developers.conexteo.com/cr%C3%A9ation-du-mod%C3%A8le-24126529e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Model name. |
| `content` | body | `string` | yes | Message content. |
| `sender` | body | `string` | yes | Default sender for the model. |
