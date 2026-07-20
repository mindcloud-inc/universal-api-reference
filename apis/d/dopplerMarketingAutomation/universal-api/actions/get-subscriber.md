# Doppler Marketing Automation: Get Subscriber

Retrieves a subscriber from Doppler Marketing Automation.

```
GET https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Marketing Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&email=subscriber%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "subscriber@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/get-subscriber?${params}`, {
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
| `email` | string | yes | Subscriber email address. Example: `subscriber@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": [
        {}
      ],
      "belongsToLists": [
        "string"
      ],
      "canBeReactivated": true,
      "email": "ava@example.com",
      "fields": [
        {}
      ],
      "isBeingReactivated": true,
      "manualUnsubscriptionReason": "string",
      "score": 1,
      "status": "string",
      "unsubscribedDate": "2026-05-07T12:00:00.000Z",
      "unsubscriptionComment": "string",
      "unsubscriptionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | array<object> |  |
| `belongsToLists` | array<string> |  |
| `canBeReactivated` | boolean |  |
| `email` | string |  |
| `fields` | array<object> |  |
| `isBeingReactivated` | boolean |  |
| `manualUnsubscriptionReason` | string |  |
| `score` | number |  |
| `status` | string |  |
| `unsubscribedDate` | date |  |
| `unsubscriptionComment` | string |  |
| `unsubscriptionType` | string |  |

## Native endpoint

Through the native Doppler Marketing Automation API, this operation is `GET /accounts/:accountName/subscribers/:email` (base URL `https://restapi.fromdoppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

