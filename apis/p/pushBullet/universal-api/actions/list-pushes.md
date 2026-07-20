# Pushbullet: List Pushes

Retrieves pushes from your Pushbullet account.

```
GET https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/list-pushes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/list-pushes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/list-pushes?${params}`, {
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
| `modified_after` | number | no | Unix timestamp to fetch newer pushes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "body": "string",
      "created": 1,
      "dismissed": true,
      "iden": "string",
      "modified": 1,
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `body` | string |  |
| `created` | number |  |
| `dismissed` | boolean |  |
| `iden` | string |  |
| `modified` | number |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Pushbullet API, this operation is `GET /pushes` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pushes.md) for the provider-specific parameters and requirements.

