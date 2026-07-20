# Marketing Master IO: List Google Sheets

Retrieves imported Google Sheets from Marketing Master IO.

```
GET https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-google-sheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-google-sheets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-google-sheets?${params}`, {
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
      "date_created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "sheet_id": "string",
      "sheet_name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_created` | date |  |
| `id` | string |  |
| `sheet_id` | string |  |
| `sheet_name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `GET /v1/google_sheets` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-google-sheets.md) for the provider-specific parameters and requirements.

