# ThriveDesk: Get Productivity Report



```
GET https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-productivity-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-productivity-report?connectionId=$CONNECTION_ID&inboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-productivity-report?${params}`, {
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
| `inboxId` | string | yes | The inbox ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "end_date": "2026-05-07T12:00:00.000Z",
      "metrics": {},
      "start_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Report response payload. |
| `end_date` | date | Report end date when returned. |
| `metrics` | object | Report metrics grouped by the provider. |
| `start_date` | date | Report start date when returned. |

## Native endpoint

Through the native ThriveDesk API, this operation is `GET /v1/reports/{{inboxId}}/productivity` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-productivity-report.md) for the provider-specific parameters and requirements.

