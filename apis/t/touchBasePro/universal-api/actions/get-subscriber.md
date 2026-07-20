# TouchBasePro: Get Subscriber

Retrieves subscriber details from your TouchBasePro account.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-subscriber?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-subscriber?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "consentToTrack": "string",
      "customFields": [
        [
          {}
        ]
      ],
      "date": "2026-05-07T12:00:00.000Z",
      "emailAddress": "ava@example.com",
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
| `consentToTrack` | string |  |
| `customFields[]` | array<object> |  |
| `customFields[].key` | string |  |
| `customFields[].value` | string |  |
| `date` | date |  |
| `emailAddress` | string |  |
| `name` | string |  |
| `readsEmailWith` | string |  |
| `state` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/subscribers/{listId}?email={email}&includetrackingpreference={includetrackingpreference}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

