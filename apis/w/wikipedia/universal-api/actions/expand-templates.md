# Wikipedia: Expand Templates

Expands templates in Wikipedia wikitext content.

```
GET https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/expand-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wikipedia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/expand-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/expand-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "expandtemplates": {},
      "warnings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expandtemplates` | object | Expanded template output from the Wikipedia API. |
| `warnings` | object | Template expansion warnings returned by the API. |

## Native endpoint

Through the native Wikipedia API, this operation is `GET /w/api.php?action=expandtemplates&prop=wikitext&format=json` (base URL `https://en.wikipedia.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/expand-templates.md) for the provider-specific parameters and requirements.

