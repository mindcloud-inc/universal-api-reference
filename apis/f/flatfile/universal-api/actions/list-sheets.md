# Flatfile: List Sheets

Retrieves a list of sheets from Flatfile.

```
GET https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/list-sheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/list-sheets?connectionId=$CONNECTION_ID&workbookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workbookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/list-sheets?${params}`, {
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
| `workbookId` | string | yes | Flatfile workbook ID to list sheets for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> | Sheet list. |

## Native endpoint

Through the native Flatfile API, this operation is `GET /sheets` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sheets.md) for the provider-specific parameters and requirements.

