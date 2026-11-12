# 3E Protect: Set Catalog Item Custom Values



```
PUT https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/set-catalog-item-custom-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/set-catalog-item-custom-values" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "string",
  "identifier": "string",
  "customValues[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/set-catalog-item-custom-values', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "string",
    "identifier": "string",
    "customValues[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source` | string | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | string | yes | Your product identifier value for the selected source. |
| `customValues[]` | array<object> | yes | Customer-defined product fields, each supplied as a name and value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customValues[].name` | string | no |  |
| `customValues[].value` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `PUT /catalog-item/customvalue/:source/:identifier` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-catalog-item-custom-values.md) for the provider-specific parameters and requirements.

