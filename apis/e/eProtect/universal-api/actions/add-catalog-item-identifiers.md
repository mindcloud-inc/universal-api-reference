# 3E Protect: Add Catalog Item Identifiers



```
PUT https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/add-catalog-item-identifiers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/add-catalog-item-identifiers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "string",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/add-catalog-item-identifiers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "string",
    "identifier": "string"
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceIdentifiers[]` | array<object> | no | Product identifier pairs to add, each with a source name and identifier value. |
| `sourceIdentifiers[].source` | string | no | Exact, case-sensitive product identifier source name agreed with 3E. |
| `sourceIdentifiers[].identifier` | string | no | Your product identifier value for the selected source. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `PUT /catalog-item/productidentifier/:source/:identifier` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-catalog-item-identifiers.md) for the provider-specific parameters and requirements.

