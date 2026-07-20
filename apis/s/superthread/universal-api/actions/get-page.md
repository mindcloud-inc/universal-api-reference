# Superthread: Get Page



```
GET https://connect.mindcloud.co/v1/universal/superthread/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superthread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superthread/latest/actions/get-page?connectionId=$CONNECTION_ID&pageId=string&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string",
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superthread/latest/actions/get-page?${params}`, {
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
| `pageId` | string | yes | Page ID to retrieve. |
| `teamId` | string | yes | Workspace ID for the Superthread workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | object |  |

## Native endpoint

Through the native Superthread API, this operation is `GET /:team_id/pages/:page_id` (base URL `https://api.superthread.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

