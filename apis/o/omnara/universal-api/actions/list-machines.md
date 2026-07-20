# Omnara: List Machines



```
GET https://connect.mindcloud.co/v1/universal/omnara/latest/actions/list-machines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/list-machines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnara/latest/actions/list-machines?${params}`, {
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
      "machines": [
        {
          "architecture": "string",
          "createdAt": "string",
          "daemonVersion": "string",
          "hostname": "Ava Chen",
          "id": "string",
          "lastSeenAt": "string",
          "metadata": {},
          "name": "Ava Chen",
          "platform": "string",
          "status": "string",
          "updatedAt": "string"
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
| `machines` | array<object> |  |
| `machines[]` | object |  |
| `machines[].architecture` | string |  |
| `machines[].createdAt` | string |  |
| `machines[].daemonVersion` | string |  |
| `machines[].hostname` | string |  |
| `machines[].id` | string |  |
| `machines[].lastSeenAt` | string |  |
| `machines[].metadata` | object |  |
| `machines[].name` | string |  |
| `machines[].platform` | string |  |
| `machines[].status` | string |  |
| `machines[].updatedAt` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `GET /api/v1/machines` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-machines.md) for the provider-specific parameters and requirements.

