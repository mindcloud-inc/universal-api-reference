# SuperSend: Get Deliverability Summary

Retrieves the deliverability summary from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-deliverability-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-deliverability-summary?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-deliverability-summary?${params}`, {
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
| `teamId` | string | yes | Team UUID (from list teams) |
| `windowDays` | number | no | Days to look back (1-90, default 30) Range: 1 to 90. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounceByProvider": {},
      "placement": {},
      "recommendations": {},
      "summary": {},
      "targetMix": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounceByProvider` | object |  |
| `placement` | object |  |
| `recommendations` | object |  |
| `summary` | object |  |
| `targetMix` | object |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /intelligence/deliverability-summary` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deliverability-summary.md) for the provider-specific parameters and requirements.

