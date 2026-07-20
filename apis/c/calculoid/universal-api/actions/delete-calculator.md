# Calculoid: Delete Calculator



```
DELETE https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/delete-calculator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/delete-calculator?connectionId=$CONNECTION_ID&calculatorId=109359" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calculatorId": "109359"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/delete-calculator?${params}`, {
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
| `calculatorId` | string | yes | Calculoid calculator ID to delete. Default: `0`. Example: `109359`. |

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
      "deleted": true,
      "id": 1
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
| `id` | number |  |

## Native endpoint

Through the native Calculoid API, this operation is `POST /calculator/delete/:calculatorId` (base URL `https://api.calculoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-calculator.md) for the provider-specific parameters and requirements.

