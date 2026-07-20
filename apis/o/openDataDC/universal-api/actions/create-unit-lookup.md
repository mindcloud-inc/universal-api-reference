# Open Data DC: Create Unit Lookup



```
POST https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-unit-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-unit-lookup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "marid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-unit-lookup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "marid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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

Through the native Open Data DC API, this operation is `POST /api/v2.2/units` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-unit-lookup.md) for the provider-specific parameters and requirements.

