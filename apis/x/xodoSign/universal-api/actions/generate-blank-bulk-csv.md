# Xodo Sign: Generate Blank Bulk CSV

Retrieves a blank bulk sending CSV for a template in Xodo Sign.

```
GET https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/generate-blank-bulk-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/generate-blank-bulk-csv?connectionId=$CONNECTION_ID&business_id=string&templateHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "business_id": "string",
  "templateHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/generate-blank-bulk-csv?${params}`, {
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
| `business_id` | string | yes | The Xodo Sign business ID that owns the template. |
| `templateHash` | string | yes | The template hash to use for bulk sending CSV generation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "csv_content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `csv_content` | string | Blank CSV structure in text format for the selected bulk-send template. |

## Native endpoint

Through the native Xodo Sign API, this operation is `GET /template/:templateHash/bulk/csv/blank` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-blank-bulk-csv.md) for the provider-specific parameters and requirements.

