# KYVE: Get Last Tokenize Share Record ID



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-last-tokenize-share-record-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-last-tokenize-share-record-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-last-tokenize-share-record-id?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/liquid/v1beta1/last_tokenize_share_record_id` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-last-tokenize-share-record-id.md) for the provider-specific parameters and requirements.

