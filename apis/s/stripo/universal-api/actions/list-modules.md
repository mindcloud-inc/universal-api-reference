# Stripo: List Modules

Retrieves saved modules from Stripo.

```
GET https://connect.mindcloud.co/v1/universal/stripo/latest/actions/list-modules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/list-modules?connectionId=$CONNECTION_ID&parameters=JSON%20object%20string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parameters": "JSON object string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripo/latest/actions/list-modules?${params}`, {
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
| `parameters` | string | yes | JSON object string for the documented module search parameters. Example: `JSON object string`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Matching Stripo modules. |
| `total` | number | Total matching module count. |

## Native endpoint

Through the native Stripo API, this operation is `GET /modules` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-modules.md) for the provider-specific parameters and requirements.

