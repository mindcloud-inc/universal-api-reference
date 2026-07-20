# AnnounceKit: Get Active Project

Retrieves the active project from AnnounceKit.

```
GET https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/get-active-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnnounceKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/get-active-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/get-active-project?${params}`, {
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
| `id` | string | AnnounceKit project id. |
| `name` | string | AnnounceKit active project name. |

## Native endpoint

Through the native AnnounceKit API, this operation is `POST /gq/v2` (base URL `https://announcekit.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-active-project.md) for the provider-specific parameters and requirements.

