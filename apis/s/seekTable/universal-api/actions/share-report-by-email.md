# SeekTable: Share Report By Email

Shares a SeekTable report by email.

```
POST https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/share-report-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/share-report-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reportId": "b1fcc6be555b4cca91843c86a414da77",
  "to": "apps@mindcloud.co",
  "subject": "SeekTable API Test"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/share-report-by-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reportId": "b1fcc6be555b4cca91843c86a414da77",
    "to": "apps@mindcloud.co",
    "subject": "SeekTable API Test"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportId` | string | yes | GUID of the report saved in your SeekTable account. Example: `b1fcc6be555b4cca91843c86a414da77`. |
| `to` | string | yes | Email address of the recipient. Example: `apps@mindcloud.co`. |
| `subject` | string | yes | Email subject line. Example: `SeekTable API Test`. |
| `message` | string | no | Additional text included in the email body. Example: `This is a MindCloud test email from the SeekTable connector.`. |
| `includeReportHtml` | boolean | no | Whether the report HTML should be included directly in the email body. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachExport` | string | no | Comma-separated list of export types to attach to the email. Example: `pdf,csv`. |
| `reportParameters` | string | no | JSON object string with report parameter values. Requires Advanced Publishing. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SeekTable API returns.

## Native endpoint

Through the native SeekTable API, this operation is `POST /api/report/:report_id/share/email` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/share-report-by-email.md) for the provider-specific parameters and requirements.

