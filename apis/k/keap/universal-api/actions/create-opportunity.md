# Keap: Create Opportunity



```
POST https://connect.mindcloud.co/v1/universal/keap/latest/actions/create-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/keap/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "opportunity_title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keap/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "opportunity_title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `affiliate_id` | string | no | Affiliate id |
| `contact_id` | string | no | Related contact id |
| `custom_fields` | string | no |  |
| `estimated_close_time` | string | no |  |
| `include_in_forecast` | string | no |  |
| `next_action_notes` | string | no |  |
| `next_action_time` | string | no |  |
| `opportunity_notes` | string | no |  |
| `opportunity_title` | string | yes | Opportunity title |
| `projected_revenue_high` | string | no |  |
| `projected_revenue_low` | string | no |  |
| `stage_id` | string | no | Opportunity stage id |
| `user_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": "string",
      "contact": {
        "companyName": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "jobTitle": "string",
        "lastName": "Chen",
        "phoneNumber": "string"
      },
      "createdTime": "string",
      "customFields": [
        {
          "content": "string",
          "id": "string"
        }
      ],
      "estimatedCloseTime": "string",
      "id": "string",
      "includeInForecast": "string",
      "lastUpdatedTime": "string",
      "nextActionNotes": "string",
      "nextActionTime": "string",
      "opportunityNotes": "string",
      "opportunityTitle": "string",
      "projectedRevenueHigh": "string",
      "projectedRevenueLow": "string",
      "stage": {
        "details": {
          "checklistItems": [
            {
              "description": "string",
              "doneDate": "2026-05-07T12:00:00.000Z",
              "id": "string",
              "instanceId": "string",
              "itemOrder": "string",
              "required": "string"
            }
          ],
          "probability": "string",
          "stageOrder": "string",
          "targetNumDays": "string"
        },
        "id": "string",
        "name": "Ava Chen",
        "reasons": [
          "string"
        ]
      },
      "user": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | string |  |
| `contact.companyName` | string |  |
| `contact.email` | string |  |
| `contact.firstName` | string |  |
| `contact.id` | string |  |
| `contact.jobTitle` | string |  |
| `contact.lastName` | string |  |
| `contact.phoneNumber` | string |  |
| `createdTime` | string |  |
| `customFields[].content` | string |  |
| `customFields[].id` | string |  |
| `estimatedCloseTime` | string |  |
| `id` | string |  |
| `includeInForecast` | string |  |
| `lastUpdatedTime` | string |  |
| `nextActionNotes` | string |  |
| `nextActionTime` | string |  |
| `opportunityNotes` | string |  |
| `opportunityTitle` | string |  |
| `projectedRevenueHigh` | string |  |
| `projectedRevenueLow` | string |  |
| `stage.details.checklistItems[].description` | string |  |
| `stage.details.checklistItems[].doneDate` | date |  |
| `stage.details.checklistItems[].id` | string |  |
| `stage.details.checklistItems[].instanceId` | string |  |
| `stage.details.checklistItems[].itemOrder` | string |  |
| `stage.details.checklistItems[].required` | string |  |
| `stage.details.probability` | string |  |
| `stage.details.stageOrder` | string |  |
| `stage.details.targetNumDays` | string |  |
| `stage.id` | string |  |
| `stage.name` | string |  |
| `stage.reasons[]` | string |  |
| `user.firstName` | string |  |
| `user.id` | string |  |
| `user.lastName` | string |  |

## Native endpoint

Through the native Keap API, this operation is `POST /opportunities` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity.md) for the provider-specific parameters and requirements.

