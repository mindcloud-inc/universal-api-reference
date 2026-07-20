# Sisense: Get Extract Datamodel Security Rules

Retrieves extract datamodel security rules from Sisense.

```
GET https://connect.mindcloud.co/v1/universal/sisense/latest/actions/get-extract-datamodel-security-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/get-extract-datamodel-security-rules?connectionId=$CONNECTION_ID&server=string&elasticube=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "server": "string",
  "elasticube": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sisense/latest/actions/get-extract-datamodel-security-rules?${params}`, {
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
| `server` | string | yes |  |
| `elasticube` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `GET /api/elasticubes/:server/:elasticube/datasecurity` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extract-datamodel-security-rules.md) for the provider-specific parameters and requirements.

