# <img src="https://images.mindcloud.co/apps/icons/images-3_1774554847204.png" alt="Crazy Egg logo" width="28" height="28"> Crazy Egg: Universal API

Crazy Egg snapshot management and conversion tracking wrapper.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/crazyEgg/latest
- **Category:** Marketing
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.crazyegg.com/
- **Vendor API docs:** https://support.crazyegg.com/knowledge-base/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Authenticate API Signature](actions/authenticate-api-signature.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/authenticate-api-signature?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Api Status

| Action | Method | Description |
| --- | --- | --- |
| [Check API Status](actions/check-api-status.md) | GET |  |

### Conversion Event

| Action | Method | Description |
| --- | --- | --- |
| [Track Conversion](actions/track-conversion.md) | POST |  |

### Signature Request

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate API Signature](actions/authenticate-api-signature.md) | GET |  |

### Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Snapshot](actions/create-snapshot.md) | POST |  |
| [Get Snapshot](actions/get-snapshot.md) | GET |  |
| [Restart Snapshot](actions/restart-snapshot.md) | PUT |  |
| [Stop Snapshot](actions/stop-snapshot.md) | PUT |  |
| [Update Snapshot](actions/update-snapshot.md) | PUT |  |

### Snapshots

| Action | Method | Description |
| --- | --- | --- |
| [List Snapshots](actions/list-snapshots.md) | GET |  |

