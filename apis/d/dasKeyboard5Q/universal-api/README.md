# <img src="https://images.mindcloud.co/apps/icons/das-keyboard5q_1776264210203.png" alt="Das Keyboard 5Q logo" width="28" height="28"> Das Keyboard 5Q: Universal API

Control Das Keyboard 5Q Q Cloud keyboard signals, including creating, listing, reading, coloring, and deleting signal records for 5Q devices.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dasKeyboard5Q/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.daskeyboard.com/
- **Vendor API docs:** https://www.daskeyboard.io/q-api-doc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Signals](actions/list-signals.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/list-signals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Signal

| Action | Method | Description |
| --- | --- | --- |
| [Create Signal](actions/create-signal.md) | POST | Creates a signal in Das Keyboard 5Q. |
| [Delete Signal](actions/delete-signal.md) | DELETE | Deletes a signal from Das Keyboard 5Q. |
| [Delete Signal By Zone](actions/delete-signal-by-zone.md) | DELETE | Deletes a signal by zone ID from Das Keyboard 5Q. |
| [Get Signal By Zone](actions/get-signal-by-zone.md) | GET | Retrieves a signal by zone ID from Das Keyboard 5Q. |
| [List Device Shadow Signals](actions/list-device-shadow-signals.md) | GET | Retrieves shadow signals for a device from Das Keyboard 5Q. |
| [List Shadow Signals](actions/list-shadow-signals.md) | GET | Retrieves shadow signals from Das Keyboard 5Q. |
| [List Signals](actions/list-signals.md) | GET | Retrieves signals from Das Keyboard 5Q. |

### Signal Color

| Action | Method | Description |
| --- | --- | --- |
| [Get Signal Color By Zone](actions/get-signal-color-by-zone.md) | GET | Retrieves a signal color by zone ID from Das Keyboard 5Q. |

