# Climatiq: Get Unit Types

Retrieves available unit types from Climatiq.

```
GET https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/get-unit-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Climatiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/get-unit-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/get-unit-types?${params}`, {
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
      "unit_types": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `unit_types` | array<object> | Available unit types and their supported input units. |

## Native endpoint

Through the native Climatiq API, this operation is `GET /data/v1/unit-types` (base URL `https://api.climatiq.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-unit-types.md) for the provider-specific parameters and requirements.

