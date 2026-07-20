# Eversign: Generate Blank CSV

Downloads a blank bulk-send CSV from Eversign.

```
GET https://connect.mindcloud.co/v1/universal/eversign/latest/actions/generate-blank-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eversign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eversign/latest/actions/generate-blank-csv?connectionId=$CONNECTION_ID&templateHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eversign/latest/actions/generate-blank-csv?${params}`, {
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
| `templateHash` | string | yes |  |

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
| `data` | array<number> |  |
| `type` | string |  |

## Native endpoint

Through the native Eversign API, this operation is `GET /template/:templateHash/bulk/csv/blank` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-blank-csv.md) for the provider-specific parameters and requirements.

