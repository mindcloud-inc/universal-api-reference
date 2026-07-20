# Zoho Creator: Update Records

Updates records in a Zoho Creator report.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/update-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/update-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountOwnerName": "Ava Chen",
  "appLinkName": "https://example.com",
  "criteria": "string",
  "data": {},
  "reportLinkName": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/update-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountOwnerName": "Ava Chen",
    "appLinkName": "https://example.com",
    "criteria": "string",
    "data": {},
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
| `criteria` | string | yes | Criteria used to select records for update. |
| `data` | object | yes | Field values to update. |
| `processUntilLimit` | boolean | no | Continue processing until the limit is reached. |
| `reportLinkName` | string | yes | Zoho Creator report link name. |
| `result` | object | no | Response result preferences. |
| `skipWorkflow[]` | array<string> | no | Workflows to skip during the update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Zoho Creator response code. |
| `result` | array<object> | Results for each updated record. |

## Native endpoint

Through the native Zoho Creator API, this operation is `PATCH /data/:account_owner_name/:app_link_name/report/:report_link_name` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-records.md) for the provider-specific parameters and requirements.

