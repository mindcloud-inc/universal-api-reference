# GatherUp: Get Business

Retrieves detailed business information from GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/get-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/get-business?connectionId=$CONNECTION_ID&businessId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/get-business?${params}`, {
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
| `businessId` | number | yes | Business id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": "string",
      "city": "string",
      "communicationMethod": "string",
      "communicationSendEmail": "ava@example.com",
      "country": "string",
      "customersNotSent": "string",
      "customField": "string",
      "emailImage": "ava@example.com",
      "emailLogo": "ava@example.com",
      "errorCode": 1,
      "errorMessage": "string",
      "extraField": "string",
      "feedbackBanner": "string",
      "feedbacksReceived": "string",
      "id": 1,
      "name": "Ava Chen",
      "nps": "string",
      "organisationType": "string",
      "package": "string",
      "phone": "string",
      "shortFeedbackUrl": "https://example.com",
      "state": "string",
      "streetAddress": "string",
      "timezone": "string",
      "type": "string",
      "websiteURL": "https://example.com",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | string |  |
| `city` | string |  |
| `communicationMethod` | string |  |
| `communicationSendEmail` | string |  |
| `country` | string |  |
| `customersNotSent` | string |  |
| `customField` | string |  |
| `emailImage` | string |  |
| `emailLogo` | string |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `extraField` | string |  |
| `feedbackBanner` | string |  |
| `feedbacksReceived` | string |  |
| `id` | number |  |
| `name` | string |  |
| `nps` | string |  |
| `organisationType` | string |  |
| `package` | string |  |
| `phone` | string |  |
| `shortFeedbackUrl` | string |  |
| `state` | string |  |
| `streetAddress` | string |  |
| `timezone` | string |  |
| `type` | string |  |
| `websiteURL` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /business/get` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business.md) for the provider-specific parameters and requirements.

