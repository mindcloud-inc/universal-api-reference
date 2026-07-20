# Open Data DC: Get Zone



```
GET https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-zone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-zone?connectionId=$CONNECTION_ID&zone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-zone?${params}`, {
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

Through the native Open Data DC API, this operation is `GET /api/v2.2/zone/:zone` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zone.md) for the provider-specific parameters and requirements.

