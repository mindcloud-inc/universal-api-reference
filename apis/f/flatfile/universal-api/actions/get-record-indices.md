# Flatfile: Get Record Indices

Retrieves record indices from a Flatfile sheet.

```
GET https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/get-record-indices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/get-record-indices?connectionId=$CONNECTION_ID&ids=us_rec_mindcloud_flatfile&sheetId=us_sht_mindcloud_flatfile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "us_rec_mindcloud_flatfile",
  "sheetId": "us_sht_mindcloud_flatfile"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/get-record-indices?${params}`, {
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
| `ids` | string | yes | Comma-delimited record IDs to inspect. Default: `us_rec_mindcloud_flatfile`. |
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
| `data` | array<object> | Record index list. |

## Native endpoint

Through the native Flatfile API, this operation is `GET /sheets/:sheetId/records/indices` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record-indices.md) for the provider-specific parameters and requirements.

