# Freshworks CRM: Update Contact

Updates an existing contact in Freshworks CRM.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact.address` | string | no |  |
| `contact.campaignId` | number | no |  |
| `contact.city` | string | no |  |
| `contact.contactStatusId` | number | no |  |
| `contact.country` | string | no |  |
| `contact.customField` | object | no |  |
| `contact.customField.cfIsActive` | boolean | no |  |
| `contact.email` | string | no |  |
| `contact.emails[]` | array<object> | no |  |
| `contact.externalId` | string | no |  |
| `contact.facebook` | string | no |  |
| `contact.firstName` | string | no |  |
| `contact.jobTitle` | string | no |  |
| `contact.keyword` | string | no |  |
| `contact.lastName` | string | no |  |
| `contact.leadSourceId` | number | no |  |
| `contact.lifecycleStageId` | number | no |  |
| `contact.linkedin` | string | no |  |
| `contact.medium` | string | no |  |
| `contact.mobileNumber` | string | no |  |
| `contact.ownerId` | number | no |  |
| `contact.salesAccountId` | number | no |  |
| `contact.salesAccounts[]` | array<object> | no |  |
| `contact.salesAccounts[].id` | number | no |  |
| `contact.salesAccounts[].isPrimary` | boolean | no |  |
| `contact.state` | string | no |  |
| `contact.subscriptionStatus[]` | array<object> | no |  |
| `contact.subscriptionTypes[]` | array<object> | no |  |
| `contact.territoryId` | number | no |  |
| `contact.timeZone` | string | no |  |
| `contact.twitter` | string | no |  |
| `contact.workNumber` | string | no |  |
| `contact.zipcode` | string | no |  |
| `contactId` | number | no | Unique contact identifier. |
| `contact` | object | no | Contact fields to update. |

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
| `contact.state` | string | State. |
| `contact.time_zone` | string | Time zone. |
| `contact.twitter` | string | Twitter profile. |
| `contact.updated_at` | date | Updated timestamp. |
| `contact.work_number` | string | Work phone number. |
| `contact.zipcode` | string | ZIP or postal code. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `PUT api/contacts/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

