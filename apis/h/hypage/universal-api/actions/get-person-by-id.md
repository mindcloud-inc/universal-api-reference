# Hy.page: Get Person by ID



```
GET https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-person-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-person-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-person-by-id?${params}`, {
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
| `id` | string | yes | Person ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "address2": "string",
      "avatarUrl": "https://example.com",
      "category": "string",
      "city": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "phone": "string",
      "purchaseValue": 1,
      "signupSource": "string",
      "state": "string",
      "subscribedAt": "2026-05-07T12:00:00.000Z",
      "subscriberStatus": "string",
      "subscription": {},
      "tags": [
        "string"
      ],
      "unsubscribedAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `avatarUrl` | string |  |
| `category` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `phone` | string |  |
| `purchaseValue` | number |  |
| `signupSource` | string |  |
| `state` | string |  |
| `subscribedAt` | date |  |
| `subscriberStatus` | string |  |
| `subscription` | object |  |
| `tags` | array<string> |  |
| `unsubscribedAt` | date |  |
| `updatedAt` | date |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Hy.page API, this operation is `GET /hyax-api/v1/people/:id` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-by-id.md) for the provider-specific parameters and requirements.

