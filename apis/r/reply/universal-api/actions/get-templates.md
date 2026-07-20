# Reply: Get Templates



```
GET https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-templates?${params}`, {
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
      "communityTemplates": [
        {}
      ],
      "orgTemplates": [
        {}
      ],
      "teamTemplates": [
        {}
      ],
      "userTemplates": [
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
| `communityTemplates` | array<object> | Templates available from the Reply community. |
| `orgTemplates` | array<object> | Templates available at the organization level. |
| `teamTemplates` | array<object> | Templates shared by the team. |
| `userTemplates` | array<object> | Templates owned by the current user. |

## Native endpoint

Through the native Reply API, this operation is `GET /v1/templates` (base URL `https://api.reply.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-templates.md) for the provider-specific parameters and requirements.

