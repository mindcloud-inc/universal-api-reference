# Sapling: List Custom Mappings

Retrieves configured custom mappings from Sapling.

```
GET https://connect.mindcloud.co/v1/universal/sapling/latest/actions/list-custom-mappings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/list-custom-mappings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/list-custom-mappings?${params}`, {
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
      "custom_mappings": [
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
| `custom_mappings` | array<object> | Custom mapping entries. |

## Native endpoint

Through the native Sapling API, this operation is `GET /api/v1/custom_mapping` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-mappings.md) for the provider-specific parameters and requirements.

