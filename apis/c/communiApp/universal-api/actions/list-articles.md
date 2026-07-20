# Communi App: List Articles



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-articles?connectionId=$CONNECTION_ID&group=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-articles?${params}`, {
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
| `group` | number | yes |  |
| `search` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_loadStatus": 1,
      "_rls": 1,
      "communiApp": 1,
      "createdBy": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "group": 1,
      "id": 1,
      "image": "string",
      "messageFormatted": "string",
      "titleFormatted": "string",
      "updatedBy": 1,
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_loadStatus` | number |  |
| `_rls` | number |  |
| `communiApp` | number |  |
| `createdBy` | number |  |
| `createdOn` | date |  |
| `group` | number |  |
| `id` | number |  |
| `image` | string |  |
| `messageFormatted` | string |  |
| `titleFormatted` | string |  |
| `updatedBy` | number |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/article` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-articles.md) for the provider-specific parameters and requirements.

