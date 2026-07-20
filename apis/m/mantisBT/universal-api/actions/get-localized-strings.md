# MantisBT: Get Localized Strings

Retrieves localized strings from MantisBT by key.

```
GET https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-localized-strings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MantisBT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-localized-strings?connectionId=$CONNECTION_ID&string%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "string[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-localized-strings?${params}`, {
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
| `string[]` | array<string> | yes | One or more localization string keys to fetch Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MantisBT API returns.

## Native endpoint

Through the native MantisBT API, this operation is `GET /lang` (base URL `{{credentials.baseUrl}}/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-localized-strings.md) for the provider-specific parameters and requirements.

