# Zoho Creator: Create Bulk Read Job

Creates a bulk read job in Zoho Creator.

```
POST https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/create-bulk-read-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/create-bulk-read-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountOwnerName": "Ava Chen",
  "appLinkName": "https://example.com",
  "query": {},
  "reportLinkName": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/create-bulk-read-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountOwnerName": "Ava Chen",
    "appLinkName": "https://example.com",
    "query": {},
    "reportLinkName": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountOwnerName` | string | yes | Zoho Creator account owner name. |
| `appLinkName` | string | yes | Zoho Creator app link name. |
| `query` | object | yes | Bulk read query options including criteria, fields, and maxRecords. |
| `reportLinkName` | string | yes | Zoho Creator report link name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "details": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Zoho Creator response code. |
| `details` | object | Bulk read job details including ID and status. |

## Native endpoint

Through the native Zoho Creator API, this operation is `POST /bulk/:account_owner_name/:app_link_name/report/:report_link_name/read` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-read-job.md) for the provider-specific parameters and requirements.

