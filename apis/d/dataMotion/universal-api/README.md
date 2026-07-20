# <img src="https://images.mindcloud.co/apps/icons/favicon-datamotion-com-48x48_1778082701831.png" alt="DataMotion logo" width="28" height="28"> DataMotion: Universal API

DataMotion Secure Message Delivery lets teams send, track, and retract encrypted secure messages through DataMotion's hosted delivery API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dataMotion/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://datamotion.com/
- **Vendor API docs:** https://datamotion.com/guide-to-secure-message-delivery-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Track Secure Message](actions/track-secure-message.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/track-secure-message?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Retract Secure Message](actions/retract-secure-message.md) | DELETE | Retracts a previously sent secure message in DataMotion. |
| [Send Secure Message](actions/send-secure-message.md) | POST | Sends a secure message through DataMotion. |

### Message Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Track Secure Message](actions/track-secure-message.md) | GET | Retrieves secure message tracking details from DataMotion. |

