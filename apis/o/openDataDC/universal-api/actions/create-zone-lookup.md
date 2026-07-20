# Open Data DC: Create Zone Lookup



```
POST https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-zone-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-zone-lookup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "zone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-zone-lookup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "zone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `zone` | string | yes | Zone identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "0": {},
      "zone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `0` | object | Zone result item. |
| `zone` | object | Zone result payload. |

## Native endpoint

Through the native Open Data DC API, this operation is `POST /api/v2.2/zone/:zone` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-zone-lookup.md) for the provider-specific parameters and requirements.

