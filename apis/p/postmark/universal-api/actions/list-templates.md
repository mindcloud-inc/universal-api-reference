# Postmark: List Templates

Retrieves templates from Postmark.

```
GET https://connect.mindcloud.co/v1/universal/postmark/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/list-templates?${params}`, {
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
| `layoutTemplate` | string | no | Filter templates by layout template alias. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Templates": [
        [
          {}
        ]
      ],
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Templates[]` | array<object> |  |
| `Templates[].Active` | boolean |  |
| `Templates[].Alias` | string |  |
| `Templates[].Name` | string |  |
| `Templates[].TemplateId` | number |  |
| `TotalCount` | number |  |

## Native endpoint

Through the native Postmark API, this operation is `GET /templates` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

