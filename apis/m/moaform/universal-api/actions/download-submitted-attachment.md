# Moaform: Download Submitted Attachment

Retrieves a submitted attachment from Moaform.

```
GET https://connect.mindcloud.co/v1/universal/moaform/latest/actions/download-submitted-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moaform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moaform/latest/actions/download-submitted-attachment?connectionId=$CONNECTION_ID&formId=string&responseId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "responseId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moaform/latest/actions/download-submitted-attachment?${params}`, {
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
| `formId` | string | yes | Unique ID of the form. |
| `responseId` | string | yes | Unique ID of the response. |
| `fileId` | string | yes | Unique ID of the submitted file. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Moaform API returns.

## Native endpoint

Through the native Moaform API, this operation is `GET /forms/:formId/responses/:responseId/files/:fileId` (base URL `https://api.moaform.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-submitted-attachment.md) for the provider-specific parameters and requirements.

