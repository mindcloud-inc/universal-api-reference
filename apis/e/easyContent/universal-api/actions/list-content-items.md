# EasyContent: List Content Items

Retrieves content items from the connected EasyContent project.

```
GET https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/list-content-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/list-content-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/list-content-items?${params}`, {
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
| `page` | number | no |  |
| `perPage` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        1
      ],
      "id": 1,
      "keywords": [
        "string"
      ],
      "name": "Ava Chen",
      "notes": "string",
      "tabs": [
        {
          "fields": [
            {
              "id": 1,
              "label": "string",
              "type": 1,
              "value": "string"
            }
          ],
          "name": "Ava Chen"
        }
      ],
      "url": "https://example.com",
      "workflowStatusId": 1,
      "workflowStatusName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories[]` | number |  |
| `id` | number |  |
| `keywords[]` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `tabs[].fields[].id` | number |  |
| `tabs[].fields[].label` | string |  |
| `tabs[].fields[].type` | number |  |
| `tabs[].fields[].value` | string |  |
| `tabs[].name` | string |  |
| `url` | string |  |
| `workflowStatusId` | number |  |
| `workflowStatusName` | string |  |

## Native endpoint

Through the native EasyContent API, this operation is `GET /v2/content/content-items` (base URL `https://easycontent.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-content-items.md) for the provider-specific parameters and requirements.

