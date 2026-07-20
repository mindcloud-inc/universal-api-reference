# <img src="https://images.mindcloud.co/apps/icons/popup-maker_1775063609180.png" alt="Popup Maker logo" width="28" height="28"> Popup Maker: Universal API

Popup Maker integration built from the provider's verified connect flow and official plugin evidence. Current supported action scope is limited to the authenticated account connection handshake and popup inventory retrieval.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/popupMaker/latest
- **Category:** Marketing
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://popupmaker.com
- **Vendor API docs:** https://help.popupmaker.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Connect Account and List Popups](actions/connect-account-and-list-popups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/popupMaker/latest/actions/connect-account-and-list-popups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Connect Account and List Popups](actions/connect-account-and-list-popups.md) | GET | Retrieves connected account details and popups from Popup Maker. |

