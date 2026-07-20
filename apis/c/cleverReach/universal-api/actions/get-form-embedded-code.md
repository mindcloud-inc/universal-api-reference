# CleverReach: Get Form Embedded Code

Retrieves deprecated embedded form code from CleverReach.

```
GET https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-form-embedded-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CleverReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-form-embedded-code?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-form-embedded-code?${params}`, {
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
| `id` | string | yes | id. |
| `badget` | boolean | no | Enable Badget (Disable only for non free plans) (default: false). |
| `embedded` | boolean | no | Embedded (default: false). |
| `js` | boolean | no | Embedded JS (default: true). Default: `true`. |
| `css` | boolean | no | Embedded CSS (default: true). Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CleverReach API returns.

## Native endpoint

Through the native CleverReach API, this operation is `GET /v3/forms.json/:id/code` (base URL `https://rest.cleverreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-embedded-code.md) for the provider-specific parameters and requirements.

