# Fleetworthy: Download Report File



```
GET https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/download-report-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/download-report-file?connectionId=$CONNECTION_ID&cpFileId=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cpFileId": "550e8400-e29b-41d4-a716-446655440000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/download-report-file?${params}`, {
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
| `cpFileId` | string | yes | The UUID corresponding to a report run file. Example: `550e8400-e29b-41d4-a716-446655440000`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fleetworthy API returns.

## Native endpoint

Through the native Fleetworthy API, this operation is `GET /reporting/report-download/:cpFileId` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-report-file.md) for the provider-specific parameters and requirements.

