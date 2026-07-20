# Calculoid: List Calculator Results



```
GET https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-calculator-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculoid `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-calculator-results?connectionId=$CONNECTION_ID&limit=25&offset=0&calculatorId=109359" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "calculatorId": "109359"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-calculator-results?${params}`, {
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

Through the native Calculoid API, this operation is `GET /results/:calculatorId` (base URL `https://api.calculoid.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calculator-results.md) for the provider-specific parameters and requirements.

