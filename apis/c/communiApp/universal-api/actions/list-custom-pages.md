# Communi App: List Custom Pages



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-custom-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-custom-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-custom-pages?${params}`, {
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
| `communiApp` | number | no |  |
| `category` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_loadStatus": 1,
      "_rls": 1,
      "category": 1,
      "communiApp": 1,
      "createdBy": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "link": "https://example.com",
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
| `category` | number |  |
| `communiApp` | number |  |
| `createdBy` | number |  |
| `createdOn` | date |  |
| `id` | number |  |
| `link` | string |  |
| `titleFormatted` | string |  |
| `updatedBy` | number |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/customPage` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-pages.md) for the provider-specific parameters and requirements.

