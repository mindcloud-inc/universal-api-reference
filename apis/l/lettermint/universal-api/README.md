# <img src="https://images.mindcloud.co/apps/icons/lettermint_1775253575775.png" alt="Lettermint logo" width="28" height="28"> Lettermint: Universal API

Send transactional emails and validate Lettermint connectivity using a project sending token.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lettermint/latest
- **Category:** Communication / Email Communications
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lettermint.co
- **Vendor API docs:** https://lettermint.co/docs/api-reference/sending

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping API](actions/ping-api.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettermint/latest/actions/ping-api?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Generic

| Action | Method | Description |
| --- | --- | --- |
| [Ping API](actions/ping-api.md) | GET | Retrieves Lettermint API status and authentication check results. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Email](actions/send-email.md) | POST | Sends a single email through Lettermint. |
| [Send Multiple Emails in a Batch](actions/send-multiple-emails-in-a-batch.md) | POST | Sends multiple emails in a batch through Lettermint. |

