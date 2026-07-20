# ActivityInfo: Download Attachment

Downloads an attachment from an ActivityInfo record.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/download-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/download-attachment?connectionId=$CONNECTION_ID&formId=string&recordId=string&fieldId=string&blobId=string&filename=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "recordId": "string",
  "fieldId": "string",
  "blobId": "string",
  "filename": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/download-attachment?${params}`, {
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
| `formId` | string | yes | ActivityInfo form ID. |
| `recordId` | string | yes | ActivityInfo record ID. |
| `fieldId` | string | yes | ActivityInfo field ID. |
| `blobId` | string | yes | ActivityInfo attachment blob ID. |
| `filename` | string | yes | Filename suffix used by ActivityInfo for browser download behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string | Downloaded attachment file. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/form/:formId/record/:recordId/field/:fieldId/blob/:blobId/:filename` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-attachment.md) for the provider-specific parameters and requirements.

