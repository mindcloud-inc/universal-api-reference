# Ziflow: List Proof Activities

Retrieves proof activities from Ziflow by proof ID.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proof-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proof-activities?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proof-activities?${params}`, {
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
| `id` | string | yes | The proof ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": [
        {
          "action_maker": {
            "contact_id": "string"
          },
          "content": [
            {
              "changes": [
                {
                  "from": "string",
                  "to": "string",
                  "type": "string"
                }
              ],
              "comment_id": "string",
              "content": "string",
              "date": "2026-05-07T12:00:00.000Z",
              "folder": {
                "id": "string",
                "name": "Ava Chen"
              },
              "from": {
                "content": "string",
                "private_comment": true
              },
              "new_attachments": [
                {
                  "file_id": "string",
                  "name": "Ava Chen"
                }
              ],
              "private_comment": true,
              "property": {
                "id": "string",
                "name": "Ava Chen",
                "values": [
                  "string"
                ]
              },
              "reaction_type": "string",
              "removed_labels": [
                {
                  "label": "string",
                  "label_id": "string"
                }
              ],
              "reviewer": {
                "contact": {
                  "email": "ava@example.com"
                },
                "id": "string"
              },
              "sequence": 1,
              "stage": {
                "id": "string",
                "name": "Ava Chen"
              },
              "to": "string"
            }
          ],
          "created_date": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "type": "string"
        }
      ],
      "count": 1,
      "has_more": true,
      "page": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities[].action_maker.contact_id` | string |  |
| `activities[].content[].changes[].from` | string |  |
| `activities[].content[].changes[].to` | string |  |
| `activities[].content[].changes[].type` | string |  |
| `activities[].content[].comment_id` | string |  |
| `activities[].content[].content` | string |  |
| `activities[].content[].date` | date |  |
| `activities[].content[].folder.id` | string |  |
| `activities[].content[].folder.name` | string |  |
| `activities[].content[].from` | string |  |
| `activities[].content[].from.content` | string |  |
| `activities[].content[].from.private_comment` | boolean |  |
| `activities[].content[].new_attachments[].file_id` | string |  |
| `activities[].content[].new_attachments[].name` | string |  |
| `activities[].content[].private_comment` | boolean |  |
| `activities[].content[].property.id` | string |  |
| `activities[].content[].property.name` | string |  |
| `activities[].content[].property.values[]` | string |  |
| `activities[].content[].reaction_type` | string |  |
| `activities[].content[].removed_labels[].label` | string |  |
| `activities[].content[].removed_labels[].label_id` | string |  |
| `activities[].content[].reviewer.contact.email` | string |  |
| `activities[].content[].reviewer.id` | string |  |
| `activities[].content[].sequence` | number |  |
| `activities[].content[].stage.id` | string |  |
| `activities[].content[].stage.name` | string |  |
| `activities[].content[].to` | string |  |
| `activities[].created_date` | date |  |
| `activities[].id` | string |  |
| `activities[].type` | string |  |
| `count` | number |  |
| `has_more` | boolean |  |
| `page` | number |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /proofs/:id/activities` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-proof-activities.md) for the provider-specific parameters and requirements.

