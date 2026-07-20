# Front: List Conversations

Retrieves a list of conversations from Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversations?${params}`, {
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
| `q` | string | no | Search query object string for conversation statuses or ticket status filters. Example: `statuses=assigned,unassigned`. |
| `sortBy` | list | no | One of: `date`. Example: `date`. |
| `sortOrder` | list | no | One of: `asc`, `desc`. Example: `asc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": [
        "string"
      ],
      "createdAt": [
        1
      ],
      "id": [
        "string"
      ],
      "isPrivate": [
        true
      ],
      "links": [
        [
          "https://example.com"
        ]
      ],
      "recipient": [
        {
          "handle": [
            "string"
          ],
          "links": [
            {
              "related": [
                {
                  "contact": [
                    "https://example.com"
                  ]
                }
              ]
            }
          ],
          "name": [
            "Ava Chen"
          ],
          "role": [
            "string"
          ]
        }
      ],
      "scheduledReminders": [
        [
          "string"
        ]
      ],
      "status": [
        "string"
      ],
      "statusCategory": [
        "string"
      ],
      "statusId": [
        "string"
      ],
      "subject": [
        "string"
      ],
      "tags": [
        [
          {}
        ]
      ],
      "ticketIds": [
        [
          "string"
        ]
      ],
      "updatedAt": [
        1
      ],
      "waitingSince": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee[]` | string |  |
| `createdAt[]` | number |  |
| `id[]` | string |  |
| `isPrivate[]` | boolean |  |
| `links[]` | array<string> |  |
| `links[].related[].comments[]` | string |  |
| `links[].related[].events[]` | string |  |
| `links[].related[].followers[]` | string |  |
| `links[].related[].inboxes[]` | string |  |
| `links[].related[].lastMessage[]` | string |  |
| `links[].related[].messages[]` | string |  |
| `links[].self[]` | string |  |
| `recipient[].handle[]` | string |  |
| `recipient[].links[].related[].contact[]` | string |  |
| `recipient[].name[]` | string |  |
| `recipient[].role[]` | string |  |
| `scheduledReminders[]` | array<string> |  |
| `status[]` | string |  |
| `statusCategory[]` | string |  |
| `statusId[]` | string |  |
| `subject[]` | string |  |
| `tags[]` | array<object> |  |
| `ticketIds[]` | array<string> |  |
| `updatedAt[]` | number |  |
| `waitingSince[]` | number |  |

## Native endpoint

Through the native Front API, this operation is `GET /conversations` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

