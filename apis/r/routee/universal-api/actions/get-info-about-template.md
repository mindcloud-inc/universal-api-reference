# Routee: Get info about template

Retrieves info about template from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-info-about-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-info-about-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-info-about-template?${params}`, {
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
| `templateId` | string | yes | ID of the template uploaded in the service. Use this method to get the template ID (use either real_id or id parameter from the reply) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "category": "string",
      "category_info": [
        [
          "string"
        ]
      ],
      "created": "string",
      "full_description": "string",
      "id": "string",
      "mark": "string",
      "mark_count": "string",
      "meta_description": "string",
      "name": "Ava Chen",
      "name_slug": "Ava Chen",
      "preview": "string",
      "real_id": 1,
      "tags": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `category` | string |  |
| `category_info[]` | array |  |
| `created` | string |  |
| `full_description` | string |  |
| `id` | string |  |
| `mark` | string |  |
| `mark_count` | string |  |
| `meta_description` | string |  |
| `name` | string |  |
| `name_slug` | string |  |
| `preview` | string |  |
| `real_id` | number |  |
| `tags[]` | array |  |

## Native endpoint

Through the native Routee API, this operation is `GET /template/:templateId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-info-about-template.md) for the provider-specific parameters and requirements.

