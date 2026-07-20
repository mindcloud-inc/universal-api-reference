# Seafile: Get Library Info

Retrieves details for a Seafile library.

```
GET https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-library-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seafile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-library-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-library-info?${params}`, {
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
| `repo_id` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Seafile API returns.

## Native endpoint

Through the native Seafile API, this operation is `GET https://plus.seafile.com/api2/repos/{repo_id}/` (base URL `https://plus.seafile.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-library-info.md) for the provider-specific parameters and requirements.

