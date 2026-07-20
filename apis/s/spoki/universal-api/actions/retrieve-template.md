# Spoki: Retrieve Template

Retrieves a template by ID, with optional channel scoping for multi-WABA accounts.

```
GET https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoki `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-template?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-template?${params}`, {
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
| `id` | number | yes | The template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "customfieldSet": [
        "string"
      ],
      "id": 1,
      "integration": 1,
      "isApproved": true,
      "isFavorite": true,
      "name": "Ava Chen",
      "subcategory": "string",
      "templateGroups": [
        {}
      ],
      "templatelocalizationSet": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `customfieldSet` | array<string> |  |
| `id` | number |  |
| `integration` | number |  |
| `isApproved` | boolean |  |
| `isFavorite` | boolean |  |
| `name` | string |  |
| `subcategory` | string |  |
| `templateGroups` | array<object> |  |
| `templatelocalizationSet` | array<object> |  |

## Native endpoint

Through the native Spoki API, this operation is `GET /templates/{{id}}/` (base URL `https://api.spoki.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-template.md) for the provider-specific parameters and requirements.

