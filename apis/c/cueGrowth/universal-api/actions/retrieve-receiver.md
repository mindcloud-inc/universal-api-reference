# CueGrowth: Retrieve Receiver



```
GET https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/retrieve-receiver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CueGrowth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/retrieve-receiver?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/retrieve-receiver?${params}`, {
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
| `receiverId` | number | no | ID of the receiver. |
| `username` | string | no | LinkedIn username of the receiver. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthday": "string",
      "companies": [
        [
          "string"
        ]
      ],
      "company": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "headline": "string",
      "id": 1,
      "ims": [
        [
          "string"
        ]
      ],
      "last_name": "Chen",
      "linkedin_url": "https://example.com",
      "location": "string",
      "phone": "string",
      "photo_url": "https://example.com",
      "positions": [
        [
          "string"
        ]
      ],
      "tags": [
        [
          "string"
        ]
      ],
      "twitter_url": "https://example.com",
      "username": "Ava Chen",
      "websites": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthday` | string |  |
| `companies[]` | array<string> |  |
| `company` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `headline` | string |  |
| `id` | number |  |
| `ims[]` | array<string> |  |
| `last_name` | string |  |
| `linkedin_url` | string |  |
| `location` | string |  |
| `phone` | string |  |
| `photo_url` | string |  |
| `positions[]` | array<string> |  |
| `tags[]` | array<string> |  |
| `twitter_url` | string |  |
| `username` | string |  |
| `websites[]` | array<string> |  |

## Native endpoint

Through the native CueGrowth API, this operation is `GET /receivers/retrieve` (base URL `https://api.cuegrowth.ai/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-receiver.md) for the provider-specific parameters and requirements.

