# AlgoDocs: List Document Data Extractors

Retrieves document data extractors from AlgoDocs.

```
GET https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/list-document-data-extractors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AlgoDocs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/list-document-data-extractors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/list-document-data-extractors?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Extractor ID. |
| `name` | string | Extractor name. |

## Native endpoint

Through the native AlgoDocs API, this operation is `GET /extractors` (base URL `https://api.algodocs.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-data-extractors.md) for the provider-specific parameters and requirements.

