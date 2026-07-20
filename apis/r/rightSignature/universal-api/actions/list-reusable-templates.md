# RightSignature: List Reusable Templates

Retrieves reusable templates from your RightSignature account.

```
GET https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/list-reusable-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/list-reusable-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/list-reusable-templates?${params}`, {
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
| `search` | string | no | A search token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "reusableTemplates": [
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
| `meta` | object |  |
| `reusableTemplates` | array<string> |  |

## Native endpoint

Through the native RightSignature API, this operation is `GET /reusable_templates` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reusable-templates.md) for the provider-specific parameters and requirements.

