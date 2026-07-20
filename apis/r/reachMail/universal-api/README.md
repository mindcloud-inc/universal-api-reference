# <img src="https://images.mindcloud.co/apps/icons/reach-mail_1774988663604.png" alt="ReachMail logo" width="28" height="28"> ReachMail: Universal API

ReachMail is an email marketing platform for managing audiences, recipients, mailings, automations, reports, tags, and webhook-driven engagement workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reachMail/latest
- **Category:** Communication / Email Communications
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://reachmail.com
- **Vendor API docs:** https://services.reachmail.net/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reachMail/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from ReachMail. |

