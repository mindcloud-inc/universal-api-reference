# <img src="https://images.mindcloud.co/apps/icons/e-bxgko-h9r-rs-baf70cbschx-qm6b-m9vcpt-o00tghagdji9bulo7qj9t2kn-xbg-mm8tq2pad0pj-d9vg_1781888702393.png" alt="DotSimple logo" width="28" height="28"> DotSimple: Universal API

Plan, publish, and manage social media content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dotSimple/latest
- **Category:** Marketing
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dotsimple.io
- **Vendor API docs:** https://help.dotsimple.io/en/collections/8-api-referenz

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotSimple/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves connected social accounts from DotSimple. |

