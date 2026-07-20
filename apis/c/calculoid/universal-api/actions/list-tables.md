# Calculoid: List Tables



```
GET https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-tables?connectionId=$CONNECTION_ID&calculatorId=109359" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calculatorId": "109359"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-tables?${params}`, {
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
| `calculatorId` | string | yes | Calculoid calculator ID. Example: `109359`. |

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
      ]
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

## Native endpoint

Through the native Calculoid API, this operation is `GET /calculator/:calculatorId/tables` (base URL `https://api.calculoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tables.md) for the provider-specific parameters and requirements.

