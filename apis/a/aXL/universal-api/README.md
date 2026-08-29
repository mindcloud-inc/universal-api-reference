# <img src="https://images.mindcloud.co/apps/icons/a-xl_1787924163828.png" alt="AXL logo" width="28" height="28"> AXL: Universal API

Manage contacts, courses, products, orders, payments, and automations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aXL/latest
- **Category:** Commerce
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://axl.tech
- **Vendor API docs:** https://axl.tech/developers/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Courses](actions/get-courses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-courses?connectionId=$CONNECTION_ID&limit=25&offset=0&fields=%7Bid%2Cname%2CisPublished%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Get Certificates](actions/get-certificates.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contacts](actions/get-contacts.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET |  |

### Course Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Course Categories](actions/get-course-categories.md) | GET |  |

### Library

| Action | Method | Description |
| --- | --- | --- |
| [Get Libraries](actions/get-libraries.md) | GET |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Orders](actions/get-orders.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Courses](actions/get-courses.md) | GET |  |

### Partner Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Partner Transactions](actions/get-partner-transactions.md) | GET |  |

### Partnership Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Partnership Members](actions/get-partnership-members.md) | GET |  |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Get Payments](actions/get-payments.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Products](actions/get-products.md) | GET |  |

### Task Verification

| Action | Method | Description |
| --- | --- | --- |
| [Get Tasks](actions/get-tasks.md) | GET |  |

