# Rithum DSCO: Get Warehouses

Lists warehouses in Rithum DSCO.

```
GET https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-warehouses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum DSCO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-warehouses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-warehouses?${params}`, {
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
| `status` | string | no | Filter warehouses by status. |
| `supplierId` | string | no | Filter warehouses by supplier ID. |
| `name` | string | no | Filter warehouses by name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scrollId` | string | no | Scroll identifier for additional warehouse result pages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "scrollId": "string",
      "warehouses": [
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
| `scrollId` | string | Scroll ID for additional pages. |
| `warehouses` | array<object> | DSCO warehouses. |

## Native endpoint

Through the native Rithum DSCO API, this operation is `GET warehouse/page` (base URL `https://api.dsco.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-warehouses.md) for the provider-specific parameters and requirements.

