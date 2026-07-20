# Send Custom Trigger Event with Perfit

## Endpoint

- **Method:** `POST`
- **Path:** `https://webhooks.myperfit.net/events/customtriggers/app4/init/764ac753/a033319a`
- **Base URL:** `https://api.myperfit.com/v2`
- **Official documentation:** [Send Custom Trigger Event](https://developers.myperfit.com/custom-triggers/activacion-y-envio-de-eventos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trigger_key` | body | `string` | yes | Custom trigger event key. |
| `contact` | body | `string` | yes | Contact email address. |
| `context` | body | `object` | no | Optional JSON object for template context. |
