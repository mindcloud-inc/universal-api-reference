# TimelinesAI: List Files

Retrieves uploaded files from your TimelinesAI workspace.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-files?${params}`, {
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
      "data": [
        {
          "filename": "Ava Chen",
          "mimetype": "string",
          "size": 1,
          "uid": "string",
          "uploadedAt": "string",
          "uploadedByEmail": "ava@example.com"
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].filename` | string |  |
| `data[].mimetype` | string |  |
| `data[].size` | number |  |
| `data[].uid` | string |  |
| `data[].uploadedAt` | string |  |
| `data[].uploadedByEmail` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `GET /files` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

