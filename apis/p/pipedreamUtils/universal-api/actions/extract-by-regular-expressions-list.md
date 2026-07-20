# Pipedream Utils: Formatting - [Text] Extract by Regular Expressions List (Regex)

Extracts matches from multiple regex patterns in Pipedream Utils.

```
GET https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/extract-by-regular-expressions-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/extract-by-regular-expressions-list?connectionId=$CONNECTION_ID&key_0=string&input_0=string&regex_0=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key_0": "string",
  "input_0": "string",
  "regex_0": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/extract-by-regular-expressions-list?${params}`, {
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
| `key_0` | string | yes | The key where the extraction result for a regex will be stored |
| `input_0` | string | yes | The text you would like to find a pattern from |
| `regex_0` | string | yes | [Regular expression](https://www.w3schools.com/js/js_regexp.asp) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pipedream Utils API returns.

## Native endpoint

Through the native Pipedream Utils API, this operation is `GET` (base URL `https://pipedream.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-by-regular-expressions-list.md) for the provider-specific parameters and requirements.

