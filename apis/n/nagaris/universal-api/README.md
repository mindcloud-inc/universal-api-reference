# <img src="https://images.mindcloud.co/apps/icons/nagaris_1775827157229.png" alt="Nagaris logo" width="28" height="28"> Nagaris: Universal API

Group-first client onboarding and engagement automation for Australian accounting firms, including client groups, clients, contacts, engagements, invoices, banking, identity verification, and work kickoff workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nagaris/latest
- **Category:** Commerce / Accounting
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nagaris.com
- **Vendor API docs:** https://core.nagaris.com/api/v1/schema/redoc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Client Groups](actions/list-client-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nagaris/latest/actions/list-client-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Client Groups](actions/list-client-groups.md) | GET | Finds client groups in Nagaris by filters. |

