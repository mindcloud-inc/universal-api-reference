# Sourcegraph: List Repositories

Retrieves repositories from Sourcegraph.

```
GET https://connect.mindcloud.co/v1/universal/sourcegraph/latest/actions/list-repositories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sourcegraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sourcegraph/latest/actions/list-repositories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sourcegraph/latest/actions/list-repositories?${params}`, {
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
| `variables.query` | string | no | Optional repository search query text. |
| `variables.first` | number | no | Maximum number of repositories to return. Default: `10`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sourcegraph API returns.

## Native endpoint

Through the native Sourcegraph API, this operation is `POST /.api/graphql` (base URL `https://sourcegraph.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-repositories.md) for the provider-specific parameters and requirements.

