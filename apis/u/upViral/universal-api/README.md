# <img src="https://images.mindcloud.co/apps/icons/id13xc-tlw1-1778182417228_1778182423239.png" alt="UpViral logo" width="28" height="28"> UpViral: Universal API

Manage UpViral campaigns, contacts, and referral activity

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/upViral/latest
- **Category:** Marketing
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.upviral.com
- **Vendor API docs:** https://www.upviral.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Campaigns](actions/list-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upViral/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves all account campaigns from UpViral. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | POST | Creates a new contact in UpViral. |
| [Add Contact Points](actions/add-contact-points.md) | PUT | Updates a contact's points in UpViral. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a campaign contact from UpViral. |
| [Get Contact By Email](actions/get-contact-by-email.md) | GET | Retrieves a campaign contact from UpViral by email. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves all campaign contacts from UpViral. |
| [List Contacts By Points](actions/list-contacts-by-points.md) | GET | Retrieves campaign contacts from UpViral by points. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves campaign custom fields from UpViral. |

