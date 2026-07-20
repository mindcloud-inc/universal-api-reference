# Paperless: List Webhooks



```
GET https://connect.mindcloud.co/v1/universal/paperless/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperless/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&oauthApplicationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "oauthApplicationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperless/latest/actions/list-webhooks?${params}`, {
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
| `oauthApplicationId` | number | yes | The Paperless integration or OAuth application ID for webhook subscriptions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data` | array<object> |  |

## Native endpoint

Through the native Paperless API, this operation is `GET /webhooks` (base URL `https://app.paperless.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

