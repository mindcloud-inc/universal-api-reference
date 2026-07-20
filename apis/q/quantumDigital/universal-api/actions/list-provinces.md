# Quantum Digital: List Provinces



```
GET https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-provinces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantum Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-provinces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-provinces?${params}`, {
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
      "alt": [
        "string"
      ],
      "country": "string",
      "name": "Ava Chen",
      "short": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt` | array<string> | Alternate names for the province or state. |
| `country` | string | Country code for the province or state. |
| `name` | string | Province or state name. |
| `short` | string | Province or state code. |

## Native endpoint

Through the native Quantum Digital API, this operation is `GET /utils/provinces?countryCodes=US,CA&excludeUST=1` (base URL `https://api.quantumdigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-provinces.md) for the provider-specific parameters and requirements.

