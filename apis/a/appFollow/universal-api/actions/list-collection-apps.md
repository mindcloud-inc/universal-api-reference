# AppFollow: List Collection Apps

Retrieves apps from an AppFollow collection.

```
GET https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-collection-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AppFollow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-collection-apps?connectionId=$CONNECTION_ID&appsId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appsId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-collection-apps?${params}`, {
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
| `appsId` | number | yes | Collection ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AppFollow API returns.

## Native endpoint

Through the native AppFollow API, this operation is `GET /api/v2/account/apps/app` (base URL `https://api.appfollow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collection-apps.md) for the provider-specific parameters and requirements.

