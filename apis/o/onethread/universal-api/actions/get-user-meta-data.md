# Onethread: Get User Meta Data



```
GET https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-user-meta-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onethread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-user-meta-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-user-meta-data?${params}`, {
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
      "accounts": [
        {}
      ],
      "companies": [
        {}
      ],
      "favouriteProjectLists": [
        {}
      ],
      "labels": [
        {}
      ],
      "projects": [
        {}
      ],
      "statuses": [
        {}
      ],
      "taskAssigns": [
        {}
      ],
      "taskLabels": [
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
| `accounts` | array<object> |  |
| `companies` | array<object> |  |
| `favouriteProjectLists` | array<object> |  |
| `labels` | array<object> |  |
| `projects` | array<object> |  |
| `statuses` | array<object> |  |
| `taskAssigns` | array<object> |  |
| `taskLabels` | array<object> |  |

## Native endpoint

Through the native Onethread API, this operation is `GET /accounts/user-meta-data` (base URL `https://api.onethread.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-meta-data.md) for the provider-specific parameters and requirements.

