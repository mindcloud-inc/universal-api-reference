# Freshworks CRM: Create Contact

Creates a new contact in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact.email": "ava@example.com",
  "contact.lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact.email": "ava@example.com",
    "contact.lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | object | no | Contact payload object as documented by Freshworks CRM. |
| `contact.address` | string | no |  |
| `contact.campaignId` | number | no |  |
| `contact.city` | string | no |  |
| `contact.contactStatusId` | number | no |  |
| `contact.country` | string | no |  |
| `contact.customField` | object | no |  |
| `contact.customField.cfIsActive` | boolean | no |  |
| `contact.email` | string | yes | Primary email address. Freshworks rejects contact creation when email is blank. |
| `contact.emails[]` | array<string> | no |  |
| `contact.externalId` | string | no |  |
| `contact.facebook` | string | no |  |
| `contact.firstName` | string | no |  |
| `contact.jobTitle` | string | no |  |
| `contact.keyword` | string | no |  |
| `contact.lastName` | string | yes |  |
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
| `contact.subscriptionStatus[]` | array<string> | no |  |
| `contact.subscriptionTypes[]` | array<string> | no |  |
| `contact.territoryId` | number | no |  |
| `contact.timeZone` | string | no |  |
| `contact.twitter` | string | no |  |
| `contact.workNumber` | string | no |  |
| `contact.zipcode` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "custom_field": {
          "cf_customer_id": "string"
        },
        "display_name": "Ava Chen",
        "email": "ava@example.com",
        "emails": [
          {
            "id": 1,
            "is_primary": true,
            "value": "ava@example.com"
          }
        ],
        "first_name": "Ava",
        "id": 1,
        "is_deleted": true,
        "last_name": "Chen",
        "lead_score": 1,
        "links": {
          "conversations": "https://example.com"
        },
        "mcr_id": 1,
        "subscription_status": 1,
        "updated_at": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.created_at` | date |  |
| `contact.custom_field.cf_customer_id` | string |  |
| `contact.display_name` | string |  |
| `contact.email` | string |  |
| `contact.emails[].id` | number |  |
| `contact.emails[].is_primary` | boolean |  |
| `contact.emails[].value` | string |  |
| `contact.first_name` | string |  |
| `contact.id` | number |  |
| `contact.is_deleted` | boolean |  |
| `contact.last_name` | string |  |
| `contact.lead_score` | number |  |
| `contact.links.conversations` | string |  |
| `contact.mcr_id` | number |  |
| `contact.subscription_status` | number |  |
| `contact.updated_at` | date |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST api/contacts` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

