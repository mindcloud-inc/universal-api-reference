# Affinda: Get specific validation result

Retrieves a specific validation result from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-validation-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-validation-result?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-validation-result?${params}`, {
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
| `id` | string | yes | Validation result's ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotations": [
        1
      ],
      "document": "string",
      "id": 1,
      "message": "string",
      "passed": true,
      "ruleSlug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotations` | array<number> |  |
| `document` | string |  |
| `id` | number |  |
| `message` | string |  |
| `passed` | boolean |  |
| `ruleSlug` | string |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/validation_results/:id` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-validation-result.md) for the provider-specific parameters and requirements.

