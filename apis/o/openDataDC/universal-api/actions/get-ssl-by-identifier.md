# Open Data DC: Get SSL By Identifier



```
GET https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-ssl-by-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-ssl-by-identifier?connectionId=$CONNECTION_ID&ssl=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ssl": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-ssl-by-identifier?${params}`, {
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
| `ssl` | string | yes | Square, suffix, lot identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "FullAddress": "string",
      "Lot": "string",
      "MarId": "string",
      "Square": "string",
      "SSL": "string",
      "Suffix": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `FullAddress` | string | Full address. |
| `Lot` | string | Lot. |
| `MarId` | string | MAR identifier. |
| `Square` | string | Square. |
| `SSL` | string | Square, suffix, lot. |
| `Suffix` | string | Suffix. |

## Native endpoint

Through the native Open Data DC API, this operation is `GET /api/v2.2/ssls/:ssl` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ssl-by-identifier.md) for the provider-specific parameters and requirements.

