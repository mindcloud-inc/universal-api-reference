# Lulu: Get Cover Validation

Retrieves a cover validation record from Lulu.

```
GET https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-cover-validation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-cover-validation?connectionId=$CONNECTION_ID&id=822044" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "822044"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-cover-validation?${params}`, {
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
| `id` | number | yes | Cover validation record ID. Default: `822044`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "id": 1,
      "sourceUrl": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `id` | number |  |
| `sourceUrl` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Lulu API, this operation is `GET /validate-cover/{id}/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cover-validation.md) for the provider-specific parameters and requirements.

