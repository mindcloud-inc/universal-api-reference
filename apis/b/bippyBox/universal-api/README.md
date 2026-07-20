# <img src="https://images.mindcloud.co/apps/icons/bippy-box_1775059451458.png" alt="BippyBox logo" width="28" height="28"> BippyBox: Universal API

BippyBox lets users retrieve account-linked BippyBox data and trigger connected notification boxes from automations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bippyBox/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bippybox.io
- **Vendor API docs:** https://bippybox.io/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Data](actions/get-user-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bippyBox/latest/actions/get-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get User Data](actions/get-user-data.md) | GET | Retrieves BippyBox account data, devices, colors, and audio files. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Trigger BippyBox](actions/trigger-bippybox.md) | POST | Triggers a BippyBox device with audio and color. |

