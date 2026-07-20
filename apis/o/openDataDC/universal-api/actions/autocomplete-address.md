# Open Data DC: Autocomplete Address



```
GET https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/autocomplete-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/autocomplete-address?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/autocomplete-address?${params}`, {
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
| `address` | string | yes | Address string value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "0": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `0` | string | Autocomplete suggestion. |

## Native endpoint

Through the native Open Data DC API, this operation is `GET /api/v2.2/autocomplete/:address` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-address.md) for the provider-specific parameters and requirements.

