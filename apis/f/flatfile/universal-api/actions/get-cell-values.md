# Flatfile: Get Cell Values

Retrieves record cell values by field in Flatfile.

```
GET https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/get-cell-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/get-cell-values?connectionId=$CONNECTION_ID&distinct=true&sheetId=us_sht_mindcloud_flatfile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "distinct": "true",
  "sheetId": "us_sht_mindcloud_flatfile"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/get-cell-values?${params}`, {
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
| `distinct` | string | yes | Must be true to request distinct cell values. Default: `true`. |
| `sheetId` | string | yes | Flatfile sheet ID. Default: `us_sht_mindcloud_flatfile`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> | Cell value list. |

## Native endpoint

Through the native Flatfile API, this operation is `GET /sheets/:sheetId/cells` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cell-values.md) for the provider-specific parameters and requirements.

