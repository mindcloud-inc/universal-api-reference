# Freshworks CRM: Get Contact

Retrieves a contact from Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-contact?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | no | Unique contact identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "address": "string",
        "avatar": "string",
        "city": "string",
        "country": "string",
        "custom_field": {
          "cf_is_active": true
        },
        "display_name": "Ava Chen",
        "email": "ava@example.com",
        "facebook": "string",
        "first_name": "Ava",
        "id": 1,
        "job_title": "string",
        "keyword": "string",
        "last_contacted": "2026-05-07T12:00:00.000Z",
        "last_name": "Chen",
        "last_seen": "2026-05-07T12:00:00.000Z",
        "lead_score": 1,
        "linkedin": "https://example.com",
        "links": {
          "activities": "https://example.com",
          "conversations": "https://example.com"
        },
        "medium": "string",
        "mobile_number": "string",
        "open_deals_amount": "string",
        "sales_accounts": [
          {
            "avatar": "string",
            "id": 1,
            "is_primary": true,
            "name": "Ava Chen",
            "partial": true,
            "website": "string"
          }
        ],
        "state": "string",
        "time_zone": "string",
        "twitter": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "work_number": "string",
        "zipcode": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.address` | string | Address. |
| `contact.avatar` | string | Avatar URL. |
| `contact.city` | string | City. |
| `contact.country` | string | Country. |
| `contact.custom_field.cf_is_active` | boolean | Custom active flag. |
| `contact.display_name` | string | Display name. |
| `contact.email` | string | Primary email. |
| `contact.facebook` | string | Facebook profile. |
| `contact.first_name` | string | Contact first name. |
| `contact.id` | number | Contact identifier. |
| `contact.job_title` | string | Job title. |
| `contact.keyword` | string | Keyword. |
| `contact.last_contacted` | date | Last contacted timestamp. |
| `contact.last_name` | string | Contact last name. |
| `contact.last_seen` | date | Last seen timestamp. |
| `contact.lead_score` | number | Lead score. |
| `contact.linkedin` | string | LinkedIn profile. |
| `contact.links.activities` | string | Activities link. |
| `contact.links.conversations` | string | Conversations link. |
| `contact.medium` | string | Attribution medium. |
| `contact.mobile_number` | string | Mobile phone number. |
| `contact.open_deals_amount` | string | Open deals amount. |
| `contact.sales_accounts[].avatar` | string | Associated account avatar. |
| `contact.sales_accounts[].id` | number | Associated account id. |
| `contact.sales_accounts[].is_primary` | boolean | Primary account marker. |
| `contact.sales_accounts[].name` | string | Associated account name. |
| `contact.sales_accounts[].partial` | boolean | Partial account payload marker. |
| `contact.sales_accounts[].website` | string | Associated account website. |
| `contact.state` | string | State. |
| `contact.time_zone` | string | Time zone. |
| `contact.twitter` | string | Twitter profile. |
| `contact.updated_at` | date | Updated timestamp. |
| `contact.work_number` | string | Work phone number. |
| `contact.zipcode` | string | ZIP or postal code. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET api/contacts/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

