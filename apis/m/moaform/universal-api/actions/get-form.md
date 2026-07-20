# Moaform: Get Form

Retrieves a form from your Moaform account.

```
GET https://connect.mindcloud.co/v1/universal/moaform/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moaform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moaform/latest/actions/get-form?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moaform/latest/actions/get-form?${params}`, {
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
| `formId` | string | yes | Unique ID of the form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocks": [
        {
          "id": "string",
          "index": "string",
          "pageId": "string",
          "properties": {
            "visible": true
          },
          "type": "string"
        }
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "longId": "string",
      "name": "Ava Chen",
      "owned": true,
      "pages": [
        {
          "blocksCount": 1,
          "id": "string",
          "number": 1,
          "visible": true
        }
      ],
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "thankyouPages": [
        {
          "content": "string",
          "id": "string"
        }
      ],
      "variables": [
        {
          "formula": "string",
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "welcomePage": {
        "content": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocks` | array<object> |  |
| `blocks[].id` | string |  |
| `blocks[].index` | string |  |
| `blocks[].pageId` | string |  |
| `blocks[].properties` | object |  |
| `blocks[].properties.visible` | boolean |  |
| `blocks[].type` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `lastUpdatedAt` | date |  |
| `longId` | string |  |
| `name` | string |  |
| `owned` | boolean |  |
| `pages` | array<object> |  |
| `pages[].blocksCount` | number |  |
| `pages[].id` | string |  |
| `pages[].number` | number |  |
| `pages[].visible` | boolean |  |
| `publishedAt` | date |  |
| `status` | string |  |
| `thankyouPages` | array<object> |  |
| `thankyouPages[].content` | string |  |
| `thankyouPages[].id` | string |  |
| `variables` | array<object> |  |
| `variables[].formula` | string |  |
| `variables[].id` | string |  |
| `variables[].name` | string |  |
| `welcomePage` | object |  |
| `welcomePage.content` | string |  |

## Native endpoint

Through the native Moaform API, this operation is `GET /forms/:formId` (base URL `https://api.moaform.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

