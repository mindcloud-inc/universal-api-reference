# Caspio: Get Table Attachment Metadata

Retrieves table attachment metadata from Caspio.

```
GET https://connect.mindcloud.co/v1/universal/caspio/latest/actions/get-table-attachment-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/get-table-attachment-metadata?connectionId=$CONNECTION_ID&tableName=Ava%20Chen&attachmentFieldName=Ava%20Chen&where=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableName": "Ava Chen",
  "attachmentFieldName": "Ava Chen",
  "where": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caspio/latest/actions/get-table-attachment-metadata?${params}`, {
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
| `tableName` | string | yes | Target table name. |
| `attachmentFieldName` | string | yes | Attachment field name. |
| `where` | string | yes | SQL-like WHERE clause that selects the row holding the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": [
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
| `Result` | array<object> |  |

## Native endpoint

Through the native Caspio API, this operation is `GET /v3/tables/{tableName}/attachments/{attachmentFieldName}/fileInfo` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table-attachment-metadata.md) for the provider-specific parameters and requirements.

