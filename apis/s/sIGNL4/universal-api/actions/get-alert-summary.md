# SIGNL4: Get Alert Summary

Retrieves an alert summary from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-summary?connectionId=$CONNECTION_ID&alertId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alertId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-summary?${params}`, {
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
| `alertId` | string | yes | Id of the alert to get the summary for |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | no | Language of the requested summary |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {},
      "serviceStatus": {
        "resetAt": "2026-05-07T12:00:00.000Z",
        "statusCode": 1,
        "statusMessage": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `serviceStatus` | object |  |
| `serviceStatus.resetAt` | date |  |
| `serviceStatus.statusCode` | number |  |
| `serviceStatus.statusMessage` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/alerts/{alertId}/summary` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert-summary.md) for the provider-specific parameters and requirements.

