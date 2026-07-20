# SafetyCulture: Get Inspection Web Report Link

Retrieves an inspection web report link from SafetyCulture.

```
GET https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-inspection-web-report-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-inspection-web-report-link?connectionId=$CONNECTION_ID&auditId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auditId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-inspection-web-report-link?${params}`, {
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
| `auditId` | string | yes | The id of the inspection to retrieve a web report link for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `GET /audits/{audit_id}/web_report_link` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inspection-web-report-link.md) for the provider-specific parameters and requirements.

