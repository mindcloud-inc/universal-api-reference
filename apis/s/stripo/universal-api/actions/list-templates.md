# Stripo: List Templates

Retrieves templates from Stripo.

```
GET https://connect.mindcloud.co/v1/universal/stripo/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/list-templates?connectionId=$CONNECTION_ID&searchParameters=JSON%20object%20string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchParameters": "JSON object string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripo/latest/actions/list-templates?${params}`, {
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
| `searchParameters` | string | yes | JSON object string for the documented template search parameters. Example: `JSON object string`. |

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
| `data` | array<object> | Matching Stripo templates. |
| `total` | number | Total matching template count. |

## Native endpoint

Through the native Stripo API, this operation is `GET /templates` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

