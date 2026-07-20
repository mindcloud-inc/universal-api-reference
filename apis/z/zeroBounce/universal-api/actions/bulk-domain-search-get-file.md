# ZeroBounce: Bulk Domain Search Get File

Retrieves a bulk domain search file from ZeroBounce.

```
GET https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/bulk-domain-search-get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZeroBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/bulk-domain-search-get-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/bulk-domain-search-get-file?${params}`, {
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
| `fileId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Processed bulk domain search file bytes. |
| `type` | string | Raw response wrapper type. |

## Native endpoint

Through the native ZeroBounce API, this operation is `GET https://bulkapi.zerobounce.net/domain-search/getfile` (base URL `https://api.zerobounce.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-domain-search-get-file.md) for the provider-specific parameters and requirements.

