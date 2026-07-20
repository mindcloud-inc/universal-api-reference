# SmugMug: List User Recent Images



```
GET https://connect.mindcloud.co/v1/universal/smugMug/latest/actions/list-user-recent-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmugMug `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smugMug/latest/actions/list-user-recent-images?connectionId=$CONNECTION_ID&limit=25&offset=0&nickname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "nickname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smugMug/latest/actions/list-user-recent-images?${params}`, {
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
| `nickname` | string | yes | SmugMug account nickname. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": 1,
      "Message": "string",
      "Options": {},
      "Response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | number | Provider status code returned by SmugMug. |
| `Message` | string | Provider status message returned by SmugMug. |
| `Options` | object | Provider-declared request options and parameter metadata when returned by SmugMug. |
| `Response` | object | Raw SmugMug response payload for the requested resource or collection. |

## Native endpoint

Through the native SmugMug API, this operation is `GET /user/:nickname!recentimages` (base URL `https://api.smugmug.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-recent-images.md) for the provider-specific parameters and requirements.

