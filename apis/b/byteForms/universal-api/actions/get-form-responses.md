# ByteForms: Get Form Responses

Retrieves responses for a ByteForms form by form ID.

```
GET https://connect.mindcloud.co/v1/universal/byteForms/latest/actions/get-form-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ByteForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/byteForms/latest/actions/get-form-responses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/byteForms/latest/actions/get-form-responses?${params}`, {
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
| `after` | string | no |  |
| `before` | string | no |  |
| `formId` | string | no |  |
| `limit` | string | no |  |
| `order` | string | no |  |
| `query` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "cursor": {},
      "data": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `cursor` | object |  |
| `data` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native ByteForms API, this operation is `GET /api/form/responses/:formId` (base URL `https://api.forms.bytesuite.io/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-responses.md) for the provider-specific parameters and requirements.

