# Calculoid: Delete Table



```
DELETE https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/delete-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/delete-table?connectionId=$CONNECTION_ID&calculatorId=109359&tableId=42" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calculatorId": "109359",
  "tableId": "42"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/delete-table?${params}`, {
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
| `calculatorId` | string | yes | Calculoid calculator ID. Default: `0`. Example: `109359`. |
| `tableId` | string | yes | Calculoid table ID. Default: `0`. Example: `42`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alerts": [
        {
          "msg": "string",
          "type": "string"
        }
      ],
      "deleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alerts[].msg` | string |  |
| `alerts[].type` | string |  |
| `deleted` | boolean |  |

## Native endpoint

Through the native Calculoid API, this operation is `POST /calculator/:calculatorId/tables/:tableId/delete` (base URL `https://api.calculoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-table.md) for the provider-specific parameters and requirements.

