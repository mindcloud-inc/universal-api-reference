# Communi App: Get Group



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-group?connectionId=$CONNECTION_ID&id=88729" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "88729"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-group?${params}`, {
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
| `id` | number | yes | Default: `88729`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_loadStatus": 1,
      "_rls": 1,
      "accessType": 1,
      "communiApp": 1,
      "createdBy": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "descriptionFormatted": "string",
      "expireOn": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "picUrl": "https://example.com",
      "status": 1,
      "title": "string",
      "type": 1
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
| `accessType` | number |  |
| `communiApp` | number |  |
| `createdBy` | number |  |
| `createdOn` | date |  |
| `descriptionFormatted` | string |  |
| `expireOn` | date |  |
| `id` | number |  |
| `name` | string |  |
| `picUrl` | string |  |
| `status` | number |  |
| `title` | string |  |
| `type` | number |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/group/:id` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

