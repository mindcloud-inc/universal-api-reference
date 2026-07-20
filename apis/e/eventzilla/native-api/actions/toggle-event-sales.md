# Toggle Event Sales with Eventzilla

Updates event sales status in Eventzilla.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/togglesales`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [Toggle Event Sales](https://developer.eventzilla.net/docs/#ev_toggle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventid` | body | `number` | yes | The Eventzilla event identifier. |
| `status` | body | `boolean` | yes | Set true to publish sales or false to unpublish them. |
