# Zoho Creator: Download File from Subform

Retrieves a file from a Zoho Creator subform record.

```
GET https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/download-file-from-subform
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/download-file-from-subform?connectionId=$CONNECTION_ID&accountOwnerName=Ava%20Chen&appLinkName=https%3A%2F%2Fexample.com&fieldLinkName=https%3A%2F%2Fexample.com&recordId=string&reportLinkName=https%3A%2F%2Fexample.com&subformLinkName=https%3A%2F%2Fexample.com&subformRecordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountOwnerName": "Ava Chen",
  "appLinkName": "https://example.com",
  "fieldLinkName": "https://example.com",
  "recordId": "string",
  "reportLinkName": "https://example.com",
  "subformLinkName": "https://example.com",
  "subformRecordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/download-file-from-subform?${params}`, {
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
| `fieldLinkName` | string | yes | Zoho Creator field link name for the file field. |
| `recordId` | string | yes | Zoho Creator record ID. |
| `reportLinkName` | string | yes | Zoho Creator report link name. |
| `subformLinkName` | string | yes | Zoho Creator subform link name. |
| `subformRecordId` | string | yes | Zoho Creator subform record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Binary file bytes for the downloaded subform attachment. |
| `type` | string | Buffer type marker returned by the MindCloud raw-response runtime. |

## Native endpoint

Through the native Zoho Creator API, this operation is `GET /data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID/:subform_link_name/:field_link_name/:subform_record_ID/download` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file-from-subform.md) for the provider-specific parameters and requirements.

