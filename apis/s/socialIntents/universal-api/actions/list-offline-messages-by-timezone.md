# Social Intents: List Offline Messages By Timezone

Retrieves offline messages from Social Intents by timezone.

```
GET https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-offline-messages-by-timezone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Social Intents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-offline-messages-by-timezone?connectionId=$CONNECTION_ID&timezone=UTC" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timezone": "UTC"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-offline-messages-by-timezone?${params}`, {
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
| `timezone` | string | yes | Filter offline messages by timezone. Example: `UTC`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiStatus": "string",
      "apiStatusCode": "string",
      "apiStatusMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiStatus` | string |  |
| `apiStatusCode` | string |  |
| `apiStatusMessage` | string |  |

## Native endpoint

Through the native Social Intents API, this operation is `GET /offlinemessages` (base URL `https://www.socialintents.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-offline-messages-by-timezone.md) for the provider-specific parameters and requirements.

