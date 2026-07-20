# Soniox: Get transcriptions

Retrieves transcriptions from Soniox.

```
GET https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-transcriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soniox `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-transcriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-transcriptions?${params}`, {
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
      "nextPageCursor": "string",
      "transcriptions": [
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
| `nextPageCursor` | string | Cursor for the next page of results. |
| `transcriptions` | array<object> | Transcriptions in the Soniox account. |

## Native endpoint

Through the native Soniox API, this operation is `GET /transcriptions` (base URL `https://api.soniox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-transcriptions.md) for the provider-specific parameters and requirements.

