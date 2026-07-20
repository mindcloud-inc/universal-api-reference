# TMetric: Get Account Balance



```
GET https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-account-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-account-balance?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-account-balance?${params}`, {
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
| `accountId` | number | yes | Workspace identifier. |
| `userId` | number | no | Optional user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "month": {
        "actualSeconds": 1,
        "actualSecondsRounded": 1,
        "requiredSeconds": 1
      },
      "today": {
        "actualSeconds": 1,
        "actualSecondsRounded": 1,
        "requiredSeconds": 1
      },
      "week": {
        "actualSeconds": 1,
        "actualSecondsRounded": 1,
        "requiredSeconds": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `month.actualSeconds` | number |  |
| `month.actualSecondsRounded` | number |  |
| `month.requiredSeconds` | number |  |
| `today.actualSeconds` | number |  |
| `today.actualSecondsRounded` | number |  |
| `today.requiredSeconds` | number |  |
| `week.actualSeconds` | number |  |
| `week.actualSecondsRounded` | number |  |
| `week.requiredSeconds` | number |  |

## Native endpoint

Through the native TMetric API, this operation is `GET /accounts/:accountId/balance` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-balance.md) for the provider-specific parameters and requirements.

