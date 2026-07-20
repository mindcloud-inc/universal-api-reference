# EODHD: Get Historical Index Constituents

Retrieves historical index constituents from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-historical-index-constituents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-historical-index-constituents?connectionId=$CONNECTION_ID&indexSymbol=GSPC.INDX" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexSymbol": "GSPC.INDX"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-historical-index-constituents?${params}`, {
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
| `indexSymbol` | string | yes | EODHD index symbol, such as `GSPC.INDX`. Example: `GSPC.INDX`. |
| `from` | date | no | Start date in `YYYY-MM-DD` format. Example: `2020-01-01`. |
| `to` | date | no | End date in `YYYY-MM-DD` format. Example: `2023-01-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "components": [
        {}
      ],
      "date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `components` | array<object> | Index constituent components for the snapshot. |
| `date` | date | Constituent snapshot date. |

## Native endpoint

Through the native EODHD API, this operation is `GET /fundamentals/{indexSymbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-historical-index-constituents.md) for the provider-specific parameters and requirements.

