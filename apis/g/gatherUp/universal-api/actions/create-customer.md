# GatherUp: Create Customer

Creates a new customer in GatherUp.

```
POST https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": 1,
  "customerEmail": "ava@example.com",
  "customerFirstName": "Ava",
  "customerLastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": 1,
    "customerEmail": "ava@example.com",
    "customerFirstName": "Ava",
    "customerLastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | number | yes | Business id. |
| `customerCustomId` | string | no | Customer custom id. |
| `customerEmail` | string | yes | Customer email address. This field is required for basic plan accounts. For higher plans there is email or phone number required. |
| `customerFirstName` | string | yes | Customer first name. |
| `customerJobId` | string | no | Customer job id. |
| `customerLastName` | string | yes | Customer last name. |
| `customerPhone` | string | no | Customer mobile phone. |
| `customerTags` | string | no | Customer tags separated by comma (max length of one tag = 50 chars). |
| `delayFeedbackRequest` | number | no | 0 will send feedback immediately -> if "sendFeedbackRequest" parameter is set to 1. If you set delayFeedbackRequest to anything over 0, it will delay that many hours before the feedback request is sent. Important the Communication Preference in the customer dashboard must be set to "Manual Mode". The "delayFeedbackRequest" parameter will be ignored if set to"Automatic Mode". |
| `customerPreference` | string | no | Customer communication preference. |
| `preferenceChecking` | number | no | If the parameter is set to 0 then Customer Preference is set according to the data provided (`customerEmail` or `customerPhone`) regardless of the `customerPreference` field value. |
| `sendFeedbackRequest` | number | no | Send feedback request email to the customer right away. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": 1,
      "errorCode": 1,
      "errorMessage": "string",
      "feedbackRequestErrorCode": 1,
      "feedbackRequestErrorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | number |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `feedbackRequestErrorCode` | number |  |
| `feedbackRequestErrorMessage` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /customer/create` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

