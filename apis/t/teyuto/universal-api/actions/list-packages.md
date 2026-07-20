# Teyuto: List Packages

Retrieves all packages from a Teyuto channel.

```
GET https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/list-packages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teyuto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/list-packages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/list-packages?${params}`, {
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
| `page` | string | no | Page of packages to return |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Teyuto API returns.

## Native endpoint

Through the native Teyuto API, this operation is `GET /packages` (base URL `https://api.teyuto.tv/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-packages.md) for the provider-specific parameters and requirements.

