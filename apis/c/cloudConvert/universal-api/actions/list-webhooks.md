# CloudConvert: List Webhooks

Retrieves webhooks from your CloudConvert account.

```
GET https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudConvert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-webhooks?${params}`, {
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
| `filter.url` | string | no | Return only webhooks for a specific URL. |
| `perPage` | number | no | Number of webhooks per page. |
| `page` | number | no | Result page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "disabled": true,
      "events": [
        "string"
      ],
      "failing": true,
      "id": 1,
      "lastErrorAt": "2026-05-07T12:00:00.000Z",
      "lastResponseCode": "string",
      "links": {
        "self": "https://example.com"
      },
      "signingSecret": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `disabled` | boolean |  |
| `events` | array<string> |  |
| `failing` | boolean |  |
| `id` | number |  |
| `lastErrorAt` | date |  |
| `lastResponseCode` | string |  |
| `links.self` | string |  |
| `signingSecret` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native CloudConvert API, this operation is `GET /users/me/webhooks` (base URL `https://api.cloudconvert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

