# Wooxy: Delete Template

Deletes an existing template from Wooxy.

```
DELETE https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-template?connectionId=$CONNECTION_ID&templateId=69d68c4e4f47c8e4a60ee99f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "69d68c4e4f47c8e4a60ee99f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-template?${params}`, {
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
| `templateId` | string | yes | The Wooxy template ID. Example: `69d68c4e4f47c8e4a60ee99f`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "result": true,
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `result` | boolean |  |
| `templateId` | string |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/template/email/remove` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

