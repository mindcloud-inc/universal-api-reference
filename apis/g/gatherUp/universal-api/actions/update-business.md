# GatherUp: Update Business

Updates an existing business in GatherUp.

```
PUT https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/update-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/update-business" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": 1,
  "businessType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/update-business', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": 1,
    "businessType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `automatedEmailsPerDay` | number | no | Automatic emails per day. 0 = manual mode. |
| `businessId` | number | yes | Business id. |
| `businessName` | string | no | Business name. |
| `businessOwnerEmail` | string | no | User email. |
| `businessOwnerFirstName` | string | no | User first name. |
| `businessOwnerLastName` | string | no | User last name. |
| `businessType` | string | yes | Google business type. |
| `city` | string | no | Business city. |
| `country` | string | no | Business country code or full name. |
| `customField` | string | no | Custom ID (whitelabeled accounts only). |
| `emailImage` | string | no | Email Picture. |
| `emailLogo` | string | no | Company Logo. |
| `feedbackBanner` | string | no | Feedback Page Banner. |
| `organisationType` | string | no | Organisation type: company, corporation, non profit, school, office, practice, agency, church, restaurant, event, firm, store, dealership |
| `phone` | string | no | Mobile phone number. |
| `state` | string | no | Business state code or full name. |
| `streetAddress` | string | no | Business street address. |
| `websiteUrl` | string | no | Business website url. |
| `zip` | string | no | Business zip code. |
| `feedbackThreshold` | number | no | Defines the NPS score threshold for feedbacks received to be automatically approved to show on the testimonials widget. |
| `pageThreshold` | number | no | Defines the NPS score of what is considered positive or negative feedback. For example if set to 5 - any customer leaving an NPS score of 5 or above will be shown the positive feedback page. |
| `language` | string | no | Business language |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": 1,
      "errorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | number |  |
| `errorMessage` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /business/update` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-business.md) for the provider-specific parameters and requirements.

