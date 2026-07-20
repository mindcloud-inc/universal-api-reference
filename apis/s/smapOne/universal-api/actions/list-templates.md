# smapOne: List templates

Retrieves smap templates from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-templates?${params}`, {
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
| `filter` | string | no | Optional template filter text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "storeUrl": "https://example.com",
      "tags": [
        "string"
      ],
      "templateId": "string",
      "title": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `storeUrl` | string |  |
| `tags` | array<string> |  |
| `templateId` | string |  |
| `title` | string |  |
| `version` | string |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /intern/Templates/Smaps` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

