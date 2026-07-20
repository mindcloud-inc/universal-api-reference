# DataScope Forms: List Generated Files

Retrieves generated files from DataScope Forms.

```
GET https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-generated-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-generated-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-generated-files?${params}`, {
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
| `end` | string | no | End of the date range to fetch generated files for. |
| `start` | string | no | Start of the date range to fetch generated files for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "form_code": "string",
      "form_name": "Ava Chen",
      "id": "string",
      "type": "string",
      "url": "https://example.com",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `form_code` | string | Code of the form. |
| `form_name` | string | Name of the form. |
| `id` | string | Identifier of the generated file notification. |
| `type` | string | Type of generated file, such as PDF or Excel. |
| `url` | string | URL of the generated file. |
| `user` | string | Name or identifier of the user who generated the file. |

## Native endpoint

Through the native DataScope Forms API, this operation is `GET /external/files` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-generated-files.md) for the provider-specific parameters and requirements.

