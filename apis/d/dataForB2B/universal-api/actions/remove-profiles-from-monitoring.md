# DataForB2B: Remove Profiles From Monitoring

Removes profiles from monitoring in DataForB2B.

```
DELETE https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/remove-profiles-from-monitoring
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForB2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/remove-profiles-from-monitoring?connectionId=$CONNECTION_ID&profileIds=https%3A%2F%2Fwww.linkedin.com%2Fin%2Fsatyanadella%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileIds": "https://www.linkedin.com/in/satyanadella/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/remove-profiles-from-monitoring?${params}`, {
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
| `profileIds` | object<string> | yes | Profile URLs or profile IDs to stop monitoring. Default: `["https://www.linkedin.com/in/satyanadella/"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "removed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `removed` | number |  |

## Native endpoint

Through the native DataForB2B API, this operation is `DELETE /webhooks/profiles` (base URL `https://api.dataforb2b.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-profiles-from-monitoring.md) for the provider-specific parameters and requirements.

