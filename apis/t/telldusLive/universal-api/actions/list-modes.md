# Telldus Live!: List Modes

Retrieves your modes from Telldus Live!.

```
GET https://connect.mindcloud.co/v1/universal/telldusLive/latest/actions/list-modes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Telldus Live! `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telldusLive/latest/actions/list-modes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telldusLive/latest/actions/list-modes?${params}`, {
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
      "builtIn": true,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `builtIn` | boolean | Whether the mode is built in. |
| `id` | string | Mode ID. |
| `name` | string | Mode name. |

## Native endpoint

Through the native Telldus Live! API, this operation is `GET /json/modes/list` (base URL `https://pa-api.telldus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-modes.md) for the provider-specific parameters and requirements.

