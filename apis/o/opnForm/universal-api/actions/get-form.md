# OpnForm: Get Form

Retrieves a form from OpnForm by slug.

```
GET https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpnForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/get-form?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/get-form?${params}`, {
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
| `slug` | string | yes | Form slug or UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "properties": [
        {}
      ],
      "settings": [
        {}
      ],
      "slug": "string",
      "title": "string",
      "translations": {},
      "workspace": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `properties` | array<object> |  |
| `settings` | array<object> |  |
| `slug` | string |  |
| `title` | string |  |
| `translations` | object |  |
| `workspace` | object |  |

## Native endpoint

Through the native OpnForm API, this operation is `GET /open/forms/:slug` (base URL `https://api.opnform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

