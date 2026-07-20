# <img src="https://images.mindcloud.co/apps/icons/luxafor_1774288223388.png" alt="Luxafor logo" width="28" height="28"> Luxafor: Universal API

Control Luxafor busy lights with colors, blinking, and patterns

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/luxafor/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://luxafor.com
- **Vendor API docs:** https://luxafor.helpscoutdocs.com/article/25-webhook-api-basics-and-guidelines

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Blink Device](actions/blink-device.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/blink-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionFields.color": "red"
}'
```

## Actions (4)

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Blink Device](actions/blink-device.md) | PUT | Updates a Luxafor device by blinking it. |
| [Play Pattern](actions/play-pattern.md) | PUT | Updates a Luxafor device by playing a pattern. |
| [Set Solid Base Color](actions/set-solid-base-color.md) | PUT | Updates a Luxafor device to a preset solid color. |
| [Set Solid Custom Color](actions/set-solid-custom-color.md) | PUT | Updates a Luxafor device to a custom solid color. |

