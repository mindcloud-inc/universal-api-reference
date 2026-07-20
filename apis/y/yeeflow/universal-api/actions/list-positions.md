# Yeeflow: List Positions



```
GET https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/list-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yeeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/list-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/list-positions?${params}`, {
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
      "Data": [
        "string"
      ],
      "Message": "string",
      "Status": 1,
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Data` | array |  |
| `Message` | string |  |
| `Status` | number |  |
| `TotalCount` | number |  |

## Native endpoint

Through the native Yeeflow API, this operation is `GET /positions` (base URL `https://api.yeeflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-positions.md) for the provider-specific parameters and requirements.

