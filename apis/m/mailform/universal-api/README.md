# <img src="https://images.mindcloud.co/apps/icons/mailform_1777563797055.png" alt="Mailform logo" width="28" height="28"> Mailform: Universal API

Send physical mail and manage API orders

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailform/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mailform.io/
- **Vendor API docs:** https://www.mailform.io/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST |  |
| [Get Order](actions/get-order.md) | GET |  |

### Pricing

| Action | Method | Description |
| --- | --- | --- |
| [Get Rate](actions/get-rate.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get All Teams](actions/get-all-teams.md) | GET |  |
| [Get Team](actions/get-team.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

