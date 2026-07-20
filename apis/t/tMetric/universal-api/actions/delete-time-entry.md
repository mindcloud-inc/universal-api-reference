# TMetric: Delete Time Entry



```
DELETE https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/delete-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/delete-time-entry?connectionId=$CONNECTION_ID&accountId=1&timeEntryId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "timeEntryId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/delete-time-entry?${params}`, {
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
| `timeEntryId` | number | yes | Time entry identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "curl": "https://example.com",
        "response": {
          "status": 1,
          "statusText": "string"
        }
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.curl` | string |  |
| `meta.response.status` | number |  |
| `meta.response.statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native TMetric API, this operation is `DELETE /accounts/:accountId/timeentries/:timeEntryId` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-time-entry.md) for the provider-specific parameters and requirements.

