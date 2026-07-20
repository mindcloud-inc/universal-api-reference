# Zoho Creator: Delete Records

Deletes records from a Zoho Creator report.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/delete-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/delete-records?connectionId=$CONNECTION_ID&accountOwnerName=Ava%20Chen&appLinkName=https%3A%2F%2Fexample.com&criteria=string&reportLinkName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountOwnerName": "Ava Chen",
  "appLinkName": "https://example.com",
  "criteria": "string",
  "reportLinkName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/delete-records?${params}`, {
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
| `accountOwnerName` | string | yes | Zoho Creator account owner name. |
| `appLinkName` | string | yes | Zoho Creator app link name. |
| `criteria` | string | yes | Criteria used to select records for deletion. |
| `processUntilLimit` | boolean | no | Continue processing until the limit is reached. |
| `reportLinkName` | string | yes | Zoho Creator report link name. |
| `result` | object | no | Response result preferences. |
| `skipWorkflow[]` | array<string> | no | Workflows to skip during the deletion. |

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
| `result` | array<object> | Results for each delete attempt. |

## Native endpoint

Through the native Zoho Creator API, this operation is `DELETE /data/:account_owner_name/:app_link_name/report/:report_link_name` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records.md) for the provider-specific parameters and requirements.

