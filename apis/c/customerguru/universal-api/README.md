# <img src="https://images.mindcloud.co/apps/icons/customerguru_1775646378215.png" alt="Customer.guru logo" width="28" height="28"> Customer.guru: Universal API

Send surveys and export customer and ratings data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/customerguru/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://customer.guru
- **Vendor API docs:** https://customer.guru/api/documentation/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Export Ratings](actions/export-ratings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/export-ratings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Export Customers](actions/export-customers.md) | GET | Retrieves customers from Customer.guru. |
| [Send Survey](actions/send-survey.md) | POST | Creates a new survey send request in Customer.guru. |

### Satisfaction Responses

| Action | Method | Description |
| --- | --- | --- |
| [Export Ratings](actions/export-ratings.md) | GET | Retrieves customer ratings from Customer.guru. |

