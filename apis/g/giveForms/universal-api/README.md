# <img src="https://images.mindcloud.co/apps/icons/give-forms_1774646838396.png" alt="GiveForms logo" width="28" height="28"> GiveForms: Universal API

Create donation forms and manage nonprofit fundraising

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/giveForms/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.giveforms.com/
- **Vendor API docs:** https://www.giveforms.com/support-article/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Donations](actions/list-donations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giveForms/latest/actions/list-donations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Donation

| Action | Method | Description |
| --- | --- | --- |
| [List Donations](actions/list-donations.md) | GET | Finds donations for your organization in GiveForms. |

