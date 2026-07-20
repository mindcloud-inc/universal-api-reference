# Lulu: Get Interior Validation

Retrieves an interior validation record from Lulu.

```
GET https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-interior-validation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-interior-validation?connectionId=$CONNECTION_ID&id=822044" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "822044"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-interior-validation?${params}`, {
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
| `id` | number | yes | Interior validation record ID. Default: `822044`. |

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
      "pageCount": "string",
      "sourceUrl": "https://example.com",
      "status": "string",
      "validPodPackageIds": [
        "string"
      ]
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
| `pageCount` | string |  |
| `sourceUrl` | string |  |
| `status` | string |  |
| `validPodPackageIds` | array<string> |  |

## Native endpoint

Through the native Lulu API, this operation is `GET /validate-interior/{id}/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-interior-validation.md) for the provider-specific parameters and requirements.

