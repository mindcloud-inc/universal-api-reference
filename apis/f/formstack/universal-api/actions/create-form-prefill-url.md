# Formstack: Create Form Prefill URL

Generates a prefilled form URL in Formstack.

```
POST https://connect.mindcloud.co/v1/universal/formstack/latest/actions/create-form-prefill-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/create-form-prefill-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstack/latest/actions/create-form-prefill-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | list<number> | yes | The ID of the form. |
| `fields[]` | array<object> | no | Field IDs and values to prefill as raw prefill field objects. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `incompletePassword` | string | no | Password for prefill. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "prefilledUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `prefilledUrl` | string | URL for the prefilled form. |

## Native endpoint

Through the native Formstack API, this operation is `POST /forms/:formId/prefill` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form-prefill-url.md) for the provider-specific parameters and requirements.

