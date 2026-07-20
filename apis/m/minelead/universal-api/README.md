# <img src="https://images.mindcloud.co/apps/icons/minelead_1775243680389.png" alt="Minelead logo" width="28" height="28"> Minelead: Universal API

Find emails, verify addresses, and manage leads and recipient lists

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/minelead/latest
- **Category:** Marketing
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://minelead.io/
- **Vendor API docs:** https://api.minelead.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minelead/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List History](actions/list-history.md) | GET | Retrieves search history from your Minelead account. |

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient List](actions/create-recipient-list.md) | POST | Creates a recipient list in Minelead. |
| [List Recipient Lists](actions/list-recipient-lists.md) | GET | Retrieves recipient lists from your Minelead account. |
| [Update Recipient List](actions/update-recipient-list.md) | PUT | Updates a recipient list in Minelead by adding or removing emails. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from your Minelead account. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves details for your Minelead account. |
| [Search Company Emails](actions/search-company-emails.md) | GET | Finds company emails in Minelead by domain. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Add Lead](actions/add-lead.md) | POST | Creates a new lead in Minelead. |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes an existing lead from Minelead. |
| [Detect Disposable Email](actions/detect-disposable-email.md) | GET | Checks whether an email address is disposable in Minelead. |
| [Find Professional Email](actions/find-professional-email.md) | GET | Finds a professional email in Minelead by name and domain. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from your Minelead account. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Minelead. |
| [Validate Email](actions/validate-email.md) | GET | Validates an email address with Minelead. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Generate Tags](actions/generate-tags.md) | POST |  |

