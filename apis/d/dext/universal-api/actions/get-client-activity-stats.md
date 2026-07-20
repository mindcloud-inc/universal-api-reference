# Dext: Get Client Activity Stats

Retrieves client activity statistics from Dext.

```
GET https://connect.mindcloud.co/v1/universal/dext/latest/actions/get-client-activity-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dext `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dext/latest/actions/get-client-activity-stats?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dext/latest/actions/get-client-activity-stats?${params}`, {
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
| `clientId` | string | yes | The Dext client identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annual": [
        "string"
      ],
      "monthlyAverage": [
        "string"
      ],
      "quarterlyAverage": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annual` | array |  |
| `monthlyAverage` | array |  |
| `quarterlyAverage` | array |  |

## Native endpoint

Through the native Dext API, this operation is `GET /clients/:client_id/activity-stats` (base URL `https://api.precision.dext.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-activity-stats.md) for the provider-specific parameters and requirements.

