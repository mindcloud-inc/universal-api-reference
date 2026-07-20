# SpreadsheetWeb Hub: Delete Tag

Deletes an existing tag from SpreadsheetWeb Hub.

```
DELETE https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/delete-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/delete-tag?connectionId=$CONNECTION_ID&request.text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/delete-tag?${params}`, {
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
| `request` | object | no | Primary request payload. |
| `request.workspaceId` | string | no | SpreadsheetWeb workspace UUID. |
| `request.tagId` | string | no | SpreadsheetWeb tag UUID. |
| `request.text` | string | yes | Tag label text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | boolean |  |

## Native endpoint

Through the native SpreadsheetWeb Hub API, this operation is `POST /tags/delete` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tag.md) for the provider-specific parameters and requirements.

