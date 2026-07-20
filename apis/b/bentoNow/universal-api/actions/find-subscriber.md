# Bento Now: Find Subscriber

Finds a subscriber in Bento Now by email or UUID.

```
GET https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/find-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bento Now `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/find-subscriber?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/find-subscriber?${params}`, {
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
| `email` | string | yes |  |
| `uuid` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "cachedTagIds": [
          "string"
        ],
        "email": "ava@example.com",
        "fields": {},
        "navigationUrl": "https://example.com",
        "unsubscribedAt": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.cachedTagIds[]` | string |  |
| `attributes.email` | string |  |
| `attributes.fields` | object |  |
| `attributes.navigationUrl` | string |  |
| `attributes.unsubscribedAt` | date |  |
| `attributes.uuid` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Bento Now API, this operation is `GET /v1/fetch/subscribers` (base URL `https://app.bentonow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-subscriber.md) for the provider-specific parameters and requirements.

