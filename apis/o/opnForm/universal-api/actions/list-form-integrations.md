# OpnForm: List Form Integrations

Lists integrations for an OpnForm form.

```
GET https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/list-form-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpnForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/list-form-integrations?connectionId=$CONNECTION_ID&formId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/list-form-integrations?${params}`, {
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
| `formId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": 1,
      "logic": [
        {}
      ],
      "provider": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `id` | number |  |
| `logic` | array<object> |  |
| `provider` | string |  |
| `status` | string |  |

## Native endpoint

Through the native OpnForm API, this operation is `GET /open/forms/:formId/integrations` (base URL `https://api.opnform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-integrations.md) for the provider-specific parameters and requirements.

