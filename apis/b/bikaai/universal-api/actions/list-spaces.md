# Bika.ai: List Spaces

Retrieves spaces from Bika.ai.

```
GET https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-spaces?${params}`, {
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
      "code": 1,
      "data": [
        {
          "createBy": "Ava Chen",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "memberCount": 1,
          "name": "Ava Chen",
          "owner": "string",
          "subscription": {}
        }
      ],
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | array<object> |  |
| `data[].createBy` | string |  |
| `data[].createdAt` | date |  |
| `data[].id` | string |  |
| `data[].memberCount` | number |  |
| `data[].name` | string |  |
| `data[].owner` | string |  |
| `data[].subscription` | object |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Bika.ai API, this operation is `GET /spaces` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spaces.md) for the provider-specific parameters and requirements.

