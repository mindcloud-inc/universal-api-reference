# Caspio: Delete View Attachment

Deletes a view attachment from Caspio.

```
DELETE https://connect.mindcloud.co/v1/universal/caspio/latest/actions/delete-view-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/delete-view-attachment?connectionId=$CONNECTION_ID&viewName=Ava%20Chen&attachmentFieldName=Ava%20Chen&where=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewName": "Ava Chen",
  "attachmentFieldName": "Ava Chen",
  "where": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caspio/latest/actions/delete-view-attachment?${params}`, {
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
| `where` | string | yes | SQL-like WHERE clause that selects the row holding the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "RecordsAffected": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `RecordsAffected` | number |  |

## Native endpoint

Through the native Caspio API, this operation is `DELETE /v3/views/{viewName}/attachments/{attachmentFieldName}` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-view-attachment.md) for the provider-specific parameters and requirements.

