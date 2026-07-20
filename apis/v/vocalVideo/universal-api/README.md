# <img src="https://images.mindcloud.co/apps/icons/vocal-video_1773935161110.png" alt="Vocal Video logo" width="28" height="28"> Vocal Video: Universal API

Monitor Vocal Video responses and published videos via webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vocalVideo/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vocalvideo.com
- **Vendor API docs:** https://help.vocalvideo.com/article/23-using-the-subscription-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from Vocal Video. |

### Reply

| Action | Method | Description |
| --- | --- | --- |
| [List Replies](actions/list-replies.md) | GET | Retrieves reply samples from Vocal Video. |

### Reply Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe to Replies](actions/subscribe-to-replies.md) | POST | Creates a reply webhook subscription in Vocal Video. |
| [Unsubscribe from Replies](actions/unsubscribe-from-replies.md) | DELETE | Deletes a reply webhook subscription from Vocal Video. |

### Storyboard

| Action | Method | Description |
| --- | --- | --- |
| [List Storyboards](actions/list-storyboards.md) | GET | Retrieves storyboard samples from Vocal Video. |

### Storyboard Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe to Storyboards](actions/subscribe-to-storyboards.md) | POST | Creates a storyboard webhook subscription in Vocal Video. |
| [Unsubscribe from Storyboards](actions/unsubscribe-from-storyboards.md) | DELETE | Deletes a storyboard webhook subscription from Vocal Video. |

