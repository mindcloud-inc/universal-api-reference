# Campaign Monitor: Get Subscriber Details

Retrieves a Campaign Monitor subscriber by email address.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-subscriber-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-subscriber-details?connectionId=$CONNECTION_ID&listId=string&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-subscriber-details?${params}`, {
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
| `listId` | string | yes | Campaign Monitor list identifier. |
| `email` | string | yes | Subscriber email address. |
| `includeTrackingPreference` | boolean | no | Include subscriber consent-to-track values. Default is false. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": [
        {}
      ],
      "date": "string",
      "emailAddress": "ava@example.com",
      "listJoinedDate": "string",
      "name": "Ava Chen",
      "readsEmailWith": "ava@example.com",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | array<object> | Custom field values for the subscriber. |
| `date` | string | Subscriber activity date returned by Campaign Monitor. |
| `emailAddress` | string | Subscriber email address. |
| `listJoinedDate` | string | Date the subscriber joined the list. |
| `name` | string | Subscriber name. |
| `readsEmailWith` | string | Email client detected by Campaign Monitor. |
| `state` | string | Current subscriber state. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /subscribers/:listId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber-details.md) for the provider-specific parameters and requirements.

