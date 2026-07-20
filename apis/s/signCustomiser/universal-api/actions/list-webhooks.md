# Sign Customiser: List Webhooks

Retrieves all webhook subscriptions from Sign Customiser.

```
GET https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign Customiser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/list-webhooks?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "meta": {},
      "ownerId": 1,
      "ownerType": "string",
      "secret": "string",
      "status": "string",
      "topic": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "webhookId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `externalId` | string |  |
| `meta` | object |  |
| `ownerId` | number |  |
| `ownerType` | string |  |
| `secret` | string |  |
| `status` | string |  |
| `topic` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `webhookId` | number |  |

## Native endpoint

Through the native Sign Customiser API, this operation is `GET /api/v2/webhooks` (base URL `https://web.signcustomiser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

