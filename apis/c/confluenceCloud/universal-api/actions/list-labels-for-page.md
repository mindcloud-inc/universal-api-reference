# Confluence: List Labels For Page

Retrieves labels for a Confluence page.

```
GET https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-labels-for-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-labels-for-page?connectionId=$CONNECTION_ID&limit=25&offset=0&cloudId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "cloudId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-labels-for-page?${params}`, {
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
| `cloudId` | string | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | string | yes | ID of the Confluence page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Links": {
        "base": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Links.base` | string |  |

## Native endpoint

Through the native Confluence API, this operation is `GET /ex/confluence/:cloudId/wiki/api/v2/pages/:id/labels` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-labels-for-page.md) for the provider-specific parameters and requirements.

