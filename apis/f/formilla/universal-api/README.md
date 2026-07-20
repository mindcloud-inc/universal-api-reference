# <img src="https://images.mindcloud.co/apps/icons/formilla_1774893354093.png" alt="Formilla logo" width="28" height="28"> Formilla: Universal API

Manage live chat, chatbots, and customer messaging

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formilla/latest
- **Category:** Support / Contact Center
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.formilla.com/
- **Vendor API docs:** https://blog.formilla.com/integrate-customer-data-with-the-formilla-rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create or Update Contact (Email Required)](actions/upsert-contact-by-email.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formilla/latest/actions/upsert-contact-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "customer@example.com"
}'
```

## Actions (2)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Contact (Email Required)](actions/upsert-contact-by-email.md) | POST | Creates or updates a contact in Formilla by email address. |
| [Create or Update Contact (User ID Required)](actions/upsert-contact-by-user-id.md) | POST | Creates or updates a contact in Formilla by user ID. |

