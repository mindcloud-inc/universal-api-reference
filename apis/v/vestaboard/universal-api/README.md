# <img src="https://images.mindcloud.co/apps/icons/vestaboard_1774450627218.png" alt="Vestaboard logo" width="28" height="28"> Vestaboard: Universal API

Read and send messages on Vestaboard displays through the Vestaboard Cloud API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vestaboard/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.vestaboard.com
- **Vendor API docs:** https://docs.vestaboard.com/docs/read-write-api/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Read Current Message](actions/read-current-message.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/read-current-message?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Read Current Message](actions/read-current-message.md) | GET | Retrieves the current message from Vestaboard. |
| [Send Message](actions/send-message.md) | POST | Sends a new message to Vestaboard. |

### Transition

| Action | Method | Description |
| --- | --- | --- |
| [Get Transition](actions/get-transition.md) | GET | Retrieves transition settings from Vestaboard. |
| [Set Transition](actions/set-transition.md) | PUT | Updates transition settings in Vestaboard. |

