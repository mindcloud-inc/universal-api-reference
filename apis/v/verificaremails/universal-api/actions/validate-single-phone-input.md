# Verificaremails: Validate Single Phone Input

Retrieves a phone validation result from Verificaremails.

```
GET https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/validate-single-phone-input
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verificaremails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/validate-single-phone-input?connectionId=$CONNECTION_ID&term=34934511100" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "34934511100"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/validate-single-phone-input?${params}`, {
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
| `term` | string | yes | Phone number to validate with international prefix. Example: 34934511100. Example: `34934511100`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Verificaremails API returns.

## Native endpoint

Through the native Verificaremails API, this operation is `GET /phone/validate/single` (base URL `https://dashboard.verificaremails.com/myapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-single-phone-input.md) for the provider-specific parameters and requirements.

