# Polaria: List Webhooks

Retrieves webhooks from a Polaria brand.

```
GET https://connect.mindcloud.co/v1/universal/polaria/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polaria `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polaria/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&apiKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polaria/latest/actions/list-webhooks?${params}`, {
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
| `apiKey` | string | yes | The Polaria widget API key for the target brand. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "event": "string",
      "id": 1,
      "token": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `event` | string |  |
| `id` | number |  |
| `token` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Polaria API, this operation is `GET /widgets/[:api_key]/webhooks` (base URL `https://app.polaria.ai/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

