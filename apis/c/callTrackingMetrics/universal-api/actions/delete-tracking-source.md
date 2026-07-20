# CallTrackingMetrics: Delete Tracking Source

Deletes an existing tracking source from CallTrackingMetrics.

```
DELETE https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/delete-tracking-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/delete-tracking-source?connectionId=$CONNECTION_ID&sourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/delete-tracking-source?${params}`, {
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
| `sourceId` | string | yes | The CallTrackingMetrics tracking source ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reason": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reason` | string |  |
| `status` | string |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `DELETE /accounts/:accountId/sources/:sourceId.json` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tracking-source.md) for the provider-specific parameters and requirements.

