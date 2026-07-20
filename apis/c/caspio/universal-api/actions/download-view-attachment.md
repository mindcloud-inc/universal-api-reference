# Caspio: Download View Attachment

Downloads a view attachment from Caspio.

```
GET https://connect.mindcloud.co/v1/universal/caspio/latest/actions/download-view-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/download-view-attachment?connectionId=$CONNECTION_ID&viewName=Ava%20Chen&attachmentFieldName=Ava%20Chen&recordPkId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewName": "Ava Chen",
  "attachmentFieldName": "Ava Chen",
  "recordPkId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caspio/latest/actions/download-view-attachment?${params}`, {
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
| `viewName` | string | yes | Target view name. |
| `attachmentFieldName` | string | yes | Attachment field name. |
| `recordPkId` | string | yes | Record primary key value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Caspio API returns.

## Native endpoint

Through the native Caspio API, this operation is `GET /v3/views/{viewName}/attachments/{attachmentFieldName}/{recordPkId}` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-view-attachment.md) for the provider-specific parameters and requirements.

