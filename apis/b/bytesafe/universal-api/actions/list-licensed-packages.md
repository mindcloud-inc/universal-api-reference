# Bytesafe: List Licensed Packages

Retrieves licensed packages from a Bytesafe registry.

```
GET https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/list-licensed-packages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bytesafe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/list-licensed-packages?connectionId=$CONNECTION_ID&query=string&registryName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "registryName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/list-licensed-packages?${params}`, {
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
| `query` | string | yes | License search query, for example MIT. |
| `registryName` | string | yes | The registry name to search for licensed packages. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bytesafe API returns.

## Native endpoint

Through the native Bytesafe API, this operation is `GET /artifacts/registries/:registryName/licensed` (base URL `https://mindcloud.bytesafe.dev/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-licensed-packages.md) for the provider-specific parameters and requirements.

