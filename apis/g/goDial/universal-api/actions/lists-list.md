# GoDial: List Contact Lists

Retrieves a list of contact lists from GoDial.

```
GET https://connect.mindcloud.co/v1/universal/goDial/latest/actions/lists-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/lists-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDial/latest/actions/lists-list?${params}`, {
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
      "callScript": "string",
      "companyId": "string",
      "id": "string",
      "indiamart": {},
      "name": "Ava Chen",
      "system": true,
      "teamsId": "string",
      "twillioAudioUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callScript` | string | Call script text. |
| `companyId` | string | Owning company identifier. |
| `id` | string | List identifier. |
| `indiamart` | object | IndiaMART integration settings. |
| `name` | string | List name. |
| `system` | boolean | Whether this is a system list. |
| `teamsId` | string | Owning team identifier. |
| `twillioAudioUrl` | string | Twilio audio URL. |

## Native endpoint

Through the native GoDial API, this operation is `GET /externals/lists/list` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lists-list.md) for the provider-specific parameters and requirements.

