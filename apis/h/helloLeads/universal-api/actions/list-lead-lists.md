# HelloLeads: List Lead Lists



```
GET https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/list-lead-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelloLeads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/list-lead-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/list-lead-lists?${params}`, {
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
      "created": "string",
      "list_key": "string",
      "modified": "string",
      "name": "Ava Chen",
      "owner": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string | Provider timestamp when the list was created. |
| `list_key` | string | HelloLeads list identifier used when creating leads into a specific list. |
| `modified` | string | Provider timestamp when the list was last modified. |
| `name` | string | HelloLeads list name. |
| `owner` | string | Owner name shown by HelloLeads for the list. |

## Native endpoint

Through the native HelloLeads API, this operation is `GET lists` (base URL `https://app.helloleads.io/index.php/private/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lead-lists.md) for the provider-specific parameters and requirements.

