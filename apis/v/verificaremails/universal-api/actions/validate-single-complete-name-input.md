# Verificaremails: Validate Single Complete Name Input

Retrieves a complete name validation result from Verificaremails.

```
GET https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/validate-single-complete-name-input
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verificaremails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/validate-single-complete-name-input?connectionId=$CONNECTION_ID&term=Use%20a%20JSON%20string%20like%20%7B%22name%22%3A%22Name%22%2C%22use_first_names%22%3A1%2C%22gender%22%3A%22M%22%2C%22country%22%3A%22ES%22%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "Use a JSON string like {\"name\":\"Name\",\"use_first_names\":1,\"gender\":\"M\",\"country\":\"ES\"}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/validate-single-complete-name-input?${params}`, {
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
| `term` | string | yes | JSON object encoded as a string. Example: {"name":"Name","use_first_names":1,"gender":"M","country":"ES"}. Example: `Use a JSON string like {"name":"Name","use_first_names":1,"gender":"M","country":"ES"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Verificaremails API returns.

## Native endpoint

Through the native Verificaremails API, this operation is `GET /namecomplete/validate/single` (base URL `https://dashboard.verificaremails.com/myapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-single-complete-name-input.md) for the provider-specific parameters and requirements.

