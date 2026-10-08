# Fleetworthy: Download Latest Report



```
GET https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/download-latest-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/download-latest-report?connectionId=$CONNECTION_ID&reportDisplayId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportDisplayId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/download-latest-report?${params}`, {
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
| `reportDisplayId` | string | yes | The display identifier for the report smart tile on the user's dashboard. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fleetworthy API returns.

## Native endpoint

Through the native Fleetworthy API, this operation is `GET /reporting/report-download-latest/:reportDisplayId` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-latest-report.md) for the provider-specific parameters and requirements.

