# Ortto: Export Campaign Data



```
GET https://connect.mindcloud.co/v1/universal/ortto/latest/actions/export-campaign-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/export-campaign-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/export-campaign-data?${params}`, {
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
| `type` | string | no | Single campaign type filter. |
| `types[]` | array<string> | no | List of campaign types to return. |
| `state` | string | no | Campaign state filter. |
| `folderId` | string | no | Folder ID filter. |
| `campaignIds[]` | array<string> | no | Specific campaign IDs to return. |
| `limit` | number | no | Maximum campaigns to return. |
| `offset` | number | no | Body offset for pagination. |
| `q` | string | no | Campaign name search query. |
| `sortOrder` | string | no | Sort direction. |
| `sort` | string | no | Sort field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folderId": "string",
      "hasMore": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folderId` | string |  |
| `hasMore` | boolean |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /campaign/get-all` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-campaign-data.md) for the provider-specific parameters and requirements.

