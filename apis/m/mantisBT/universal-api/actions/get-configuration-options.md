# MantisBT: Get Configuration Options

Retrieves configuration options from MantisBT by key.

```
GET https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-configuration-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MantisBT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-configuration-options?connectionId=$CONNECTION_ID&option%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "option[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-configuration-options?${params}`, {
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
| `option[]` | array<string> | yes | One or more configuration option names to fetch Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MantisBT API returns.

## Native endpoint

Through the native MantisBT API, this operation is `GET /config` (base URL `{{credentials.baseUrl}}/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-configuration-options.md) for the provider-specific parameters and requirements.

