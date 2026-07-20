# Sourcegraph: Get Organization By Name

Retrieves an organization from Sourcegraph by name.

```
GET https://connect.mindcloud.co/v1/universal/sourcegraph/latest/actions/get-organization-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sourcegraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sourcegraph/latest/actions/get-organization-by-name?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sourcegraph/latest/actions/get-organization-by-name?${params}`, {
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
| `variables.name` | string | no | The Sourcegraph organization name to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sourcegraph API returns.

## Native endpoint

Through the native Sourcegraph API, this operation is `POST /.api/graphql` (base URL `https://sourcegraph.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-by-name.md) for the provider-specific parameters and requirements.

