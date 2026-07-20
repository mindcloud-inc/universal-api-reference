# <img src="https://images.mindcloud.co/apps/icons/pledge_1774630496359.png" alt="Pledge logo" width="28" height="28"> Pledge: Universal API

Search nonprofits, create fundraisers, and process donations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pledge/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pledge.to
- **Vendor API docs:** https://developer.pledge.to/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Fundraiser](actions/create-fundraiser.md) | POST | Creates a fundraiser in Pledge. |
| [Get Fundraiser](actions/get-fundraiser.md) | GET | Retrieves a fundraiser from Pledge. |
| [Place Fundraiser](actions/place-fundraiser.md) | PUT | Updates fundraiser placement in Pledge. |
| [Update Fundraiser](actions/update-fundraiser.md) | PUT | Updates an existing fundraiser in Pledge. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Pledge. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Pledge. |
| [Request Organization](actions/request-organization.md) | POST | Requests an organization in Pledge. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Donation](actions/create-donation.md) | POST | Creates a donation in Pledge. |
| [Get Donation](actions/get-donation.md) | GET | Retrieves a donation from Pledge. |
| [List Donations](actions/list-donations.md) | GET | Retrieves donations from Pledge. |

### Programs

| Action | Method | Description |
| --- | --- | --- |
| [Create Impact Calculator](actions/create-impact-calculator.md) | POST | Creates an impact calculator in Pledge. |
| [Get Impact Calculator](actions/get-impact-calculator.md) | GET | Retrieves an impact calculator from Pledge. |
| [List Impact Calculators](actions/list-impact-calculators.md) | GET | Retrieves impact calculators from Pledge. |
| [Update Impact Calculator](actions/update-impact-calculator.md) | PUT | Updates an impact calculator in Pledge. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | POST | Creates a webhook endpoint in Pledge. |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | DELETE | Deletes a webhook endpoint from Pledge. |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | GET | Retrieves a webhook endpoint from Pledge. |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET | Retrieves webhook endpoints from Pledge. |

