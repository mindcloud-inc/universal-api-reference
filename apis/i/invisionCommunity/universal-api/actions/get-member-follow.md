# Invision Community: Get Member Follow



```
GET https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-member-follow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invision Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-member-follow?connectionId=$CONNECTION_ID&id=1&followKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "followKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-member-follow?${params}`, {
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
| `id` | number | yes | Member identifier. |
| `followKey` | string | yes | Follow identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "perPage": 1,
      "results": [
        {}
      ],
      "totalPages": 1,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `perPage` | number |  |
| `results` | array<object> |  |
| `totalPages` | number |  |
| `totalResults` | number |  |

## Native endpoint

Through the native Invision Community API, this operation is `GET /core/members/:id/follows/:followKey` (base URL `{{credentials.communityBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member-follow.md) for the provider-specific parameters and requirements.

