# 3E Protect: Assign Catalog Item to Location by GUID



```
PUT https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/assign-catalog-item-to-location-by-guid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/assign-catalog-item-to-location-by-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cpcGuid": "string",
  "targetLocationGuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/assign-catalog-item-to-location-by-guid', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cpcGuid": "string",
    "targetLocationGuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cpcGuid` | string | yes | 3E catalog product GUID (unique record identifier). |
| `targetLocationGuid` | string | yes | Location GUID (unique record identifier) returned by List Locations. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `PUT /inventory-assignment/catalog-guid-location-identifier/:cpcGuid/:targetLocationGuid` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-catalog-item-to-location-by-guid.md) for the provider-specific parameters and requirements.

