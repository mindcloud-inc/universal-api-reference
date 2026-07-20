# Recommand: List Webhooks

Retrieves webhook records from the Recommand API.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-webhooks?${params}`, {
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
| `companyid` | string | no | companyId parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "webhooks": [
        {
          "companyId": "string",
          "createdAt": "string",
          "id": "string",
          "teamId": "string",
          "updatedAt": "string",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `webhooks` | array<object> |  |
| `webhooks[].companyId` | string |  |
| `webhooks[].createdAt` | string |  |
| `webhooks[].id` | string |  |
| `webhooks[].teamId` | string |  |
| `webhooks[].updatedAt` | string |  |
| `webhooks[].url` | string |  |

## Native endpoint

Through the native Recommand API, this operation is `GET /api/v1/webhooks` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

