# Open Data DC: Get Units By MAR ID



```
GET https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-units-by-mar-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-units-by-mar-id?connectionId=$CONNECTION_ID&marid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "marid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-units-by-mar-id?${params}`, {
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
| `marid` | string | yes | MAR identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "0": {
        "FullAddress": "string",
        "MarId": "string",
        "UnitNum": "string",
        "UnitType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `0` | object | Unit result. |
| `0.FullAddress` | string | Full address. |
| `0.MarId` | string | MAR identifier. |
| `0.UnitNum` | string | Unit number. |
| `0.UnitType` | string | Unit type. |

## Native endpoint

Through the native Open Data DC API, this operation is `GET /api/v2.2/units/:marid` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-units-by-mar-id.md) for the provider-specific parameters and requirements.

