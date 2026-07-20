# EODHD: List Supported Forex Pairs

Retrieves supported forex pairs from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-supported-forex-pairs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-supported-forex-pairs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-supported-forex-pairs?${params}`, {
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
      "Code": "string",
      "Country": "string",
      "Currency": "string",
      "Exchange": "string",
      "Name": "Ava Chen",
      "Type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string | Forex pair code. |
| `Country` | string | Country value returned by EODHD. |
| `Currency` | string | Currency value returned by EODHD. |
| `Exchange` | string | Virtual exchange code. |
| `Name` | string | Forex pair display name. |
| `Type` | string | Instrument type. |

## Native endpoint

Through the native EODHD API, this operation is `GET /exchange-symbol-list/{exchangeCode}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-forex-pairs.md) for the provider-specific parameters and requirements.

