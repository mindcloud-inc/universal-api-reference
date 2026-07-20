# Rithum DSCO: Get Catalog Object

Retrieves a catalog item from Rithum DSCO.

```
GET https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-catalog-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum DSCO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-catalog-by-id?connectionId=$CONNECTION_ID&itemKey=string&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemKey": "string",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-catalog-by-id?${params}`, {
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
| `itemKey` | string | yes | Required identifier key used to find the catalog object. |
| `value` | string | yes | Required identifier value used to find the catalog object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dscoItemId": "string",
      "sku": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dscoItemId` | string | DSCO catalog item ID. |
| `sku` | string | Catalog item SKU. |
| `title` | string | Catalog item title. |

## Native endpoint

Through the native Rithum DSCO API, this operation is `GET catalog` (base URL `https://api.dsco.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog-by-id.md) for the provider-specific parameters and requirements.

