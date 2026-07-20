# Swipe One: Create Note



```
POST https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "title": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "title": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The unique ID of the contact for which the note is created. |
| `title` | string | yes | The title of the note. |
| `content` | string | yes | The content of the note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "content": {
        "content": [
          {
            "attrs": {
              "level": 1,
              "textAlign": "string"
            },
            "content": [
              {
                "text": "string",
                "type": "string"
              }
            ],
            "type": "string"
          }
        ],
        "type": "string"
      },
      "createdAt": "string",
      "createdBy": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "Id": "string",
      "updatedAt": "string",
      "V": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `content.content[].attrs.level` | number |  |
| `content.content[].attrs.textAlign` | string |  |
| `content.content[].content[].text` | string |  |
| `content.content[].content[].type` | string |  |
| `content.content[].type` | string |  |
| `content.type` | string |  |
| `createdAt` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.type` | string |  |
| `Id` | string |  |
| `updatedAt` | string |  |
| `V` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `POST /contacts/:contactId/notes` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

