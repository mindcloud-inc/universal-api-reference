# Zeplin: List Project Design Tokens

Retrieves a list of project design tokens from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-design-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-design-tokens?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-design-tokens?${params}`, {
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
| `projectId` | string | yes | Project id |
| `includeLinkedStyleguides` | boolean | no | Whether to include linked styleguides or not |
| `tokenNameCase` | string | no | Case for token names |

## Response

```json
{
  "success": true,
  "data": [
    {
      "colors": {},
      "spacing": {},
      "text_styles": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colors` | object |  |
| `spacing` | object |  |
| `text_styles` | object |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/design_tokens` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-design-tokens.md) for the provider-specific parameters and requirements.

