# DataBridge: Retrieve Chunks Grouped

Retrieves grouped document chunks from DataBridge.

```
GET https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/retrieve-chunks-grouped
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataBridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/retrieve-chunks-grouped?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/retrieve-chunks-grouped?${params}`, {
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
      "chunks": [
        {}
      ],
      "groups": [
        {}
      ],
      "hasPadding": true,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunks` | array<object> |  |
| `groups` | array<object> |  |
| `hasPadding` | boolean |  |
| `totalResults` | number |  |

## Native endpoint

Through the native DataBridge API, this operation is `POST /retrieve/chunks/grouped` (base URL `https://api.morphik.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-chunks-grouped.md) for the provider-specific parameters and requirements.

