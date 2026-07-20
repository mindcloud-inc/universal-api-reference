# Zoho Creator: Delete Record by ID

Deletes a specific Zoho Creator record by ID.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/delete-record-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/delete-record-by-id?connectionId=$CONNECTION_ID&accountOwnerName=Ava%20Chen&appLinkName=https%3A%2F%2Fexample.com&recordId=string&reportLinkName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountOwnerName": "Ava Chen",
  "appLinkName": "https://example.com",
  "recordId": "string",
  "reportLinkName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/delete-record-by-id?${params}`, {
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
| `recordId` | string | yes | Zoho Creator record ID. |
| `reportLinkName` | string | yes | Zoho Creator report link name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Zoho Creator response code. |
| `data` | object | The deleted record reference returned by Zoho Creator. |
| `message` | string | Zoho Creator success message. |

## Native endpoint

Through the native Zoho Creator API, this operation is `DELETE /data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-record-by-id.md) for the provider-specific parameters and requirements.

