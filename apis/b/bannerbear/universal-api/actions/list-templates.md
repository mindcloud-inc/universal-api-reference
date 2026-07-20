# Bannerbear: List Templates

Retrieves templates from Bannerbear.

```
GET https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbear `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/list-templates?${params}`, {
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
| `name` | string | no | Filter templates by name. |
| `tag` | string | no | Filter templates by tag. |
| `extended` | boolean | no | Return the extended template response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannerbear API returns.

## Native endpoint

Through the native Bannerbear API, this operation is `GET /v2/templates` (base URL `https://api.bannerbear.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

