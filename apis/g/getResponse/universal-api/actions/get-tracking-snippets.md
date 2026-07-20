# GetResponse: Get Tracking Snippets

Retrieves tracking code snippets from GetResponse.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-tracking-snippets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-tracking-snippets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-tracking-snippets?${params}`, {
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
      "grid": "string",
      "snippet": "string",
      "snippetV2": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `grid` | string |  |
| `snippet` | string |  |
| `snippetV2` | string |  |

## Native endpoint

Through the native GetResponse API, this operation is `GET /tracking` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracking-snippets.md) for the provider-specific parameters and requirements.

