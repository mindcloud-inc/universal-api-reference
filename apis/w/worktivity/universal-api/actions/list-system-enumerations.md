# Worktivity: List System Enumerations

Retrieves system enumeration values from Worktivity.

```
GET https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-system-enumerations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worktivity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-system-enumerations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-system-enumerations?${params}`, {
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
      "description": "string",
      "enums": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Enumeration group description. |
| `enums` | array<object> | Available enum values for this group. |
| `title` | string | Enumeration group name. |

## Native endpoint

Through the native Worktivity API, this operation is `GET /Definition/ListEnums` (base URL `https://open-api.useworktivity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-system-enumerations.md) for the provider-specific parameters and requirements.

