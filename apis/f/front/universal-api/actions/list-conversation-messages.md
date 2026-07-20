# Front: List Conversation Messages

Retrieves a list of conversation messages from Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversation-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversation-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&conversationId=cnv_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "conversationId": "cnv_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversation-messages?${params}`, {
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
| `conversationId` | string | yes | Example: `cnv_123`. |
| `sortBy` | list | no | One of: `created_at`. Example: `created_at`. |
| `sortOrder` | list | no | One of: `asc`, `desc`. Example: `asc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        [
          "string"
        ]
      ],
      "author": [
        {
          "email": [
            "ava@example.com"
          ],
          "firstName": [
            "Ava"
          ],
          "id": [
            "string"
          ],
          "isAdmin": [
            true
          ],
          "isAvailable": [
            true
          ],
          "isBlocked": [
            true
          ],
          "lastName": [
            "Chen"
          ],
          "links": [
            {
              "related": [
                {
                  "conversations": [
                    "https://example.com"
                  ],
                  "inboxes": [
                    "https://example.com"
                  ]
                }
              ],
              "self": [
                "https://example.com"
              ]
            }
          ],
          "type": [
            "string"
          ],
          "username": [
            "Ava Chen"
          ]
        }
      ],
      "blurb": [
        "string"
      ],
      "body": [
        "string"
      ],
      "createdAt": [
        1
      ],
      "draftMode": [
        "string"
      ],
      "errorType": [
        "string"
      ],
      "id": [
        "string"
      ],
      "isDraft": [
        true
      ],
      "isInbound": [
        true
      ],
      "links": [
        {
          "related": [
            {
              "conversation": [
                "https://example.com"
              ],
              "messageRepliedTo": [
                "https://example.com"
              ],
              "messageSeen": [
                "https://example.com"
              ]
            }
          ],
          "self": [
            "https://example.com"
          ]
        }
      ],
      "messageUid": [
        "string"
      ],
      "recipients": [
        [
          {}
        ]
      ],
      "signature": [
        "string"
      ],
      "subject": [
        "string"
      ],
      "text": [
        "string"
      ],
      "type": [
        "string"
      ],
      "version": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments[]` | array<string> |  |
| `author[].email[]` | string |  |
| `author[].firstName[]` | string |  |
| `author[].id[]` | string |  |
| `author[].isAdmin[]` | boolean |  |
| `author[].isAvailable[]` | boolean |  |
| `author[].isBlocked[]` | boolean |  |
| `author[].lastName[]` | string |  |
| `author[].links[].related[].conversations[]` | string |  |
| `author[].links[].related[].inboxes[]` | string |  |
| `author[].links[].self[]` | string |  |
| `author[].type[]` | string |  |
| `author[].username[]` | string |  |
| `blurb[]` | string |  |
| `body[]` | string |  |
| `createdAt[]` | number |  |
| `draftMode[]` | string |  |
| `errorType[]` | string |  |
| `id[]` | string |  |
| `isDraft[]` | boolean |  |
| `isInbound[]` | boolean |  |
| `links[].related[].conversation[]` | string |  |
| `links[].related[].messageRepliedTo[]` | string |  |
| `links[].related[].messageSeen[]` | string |  |
| `links[].self[]` | string |  |
| `messageUid[]` | string |  |
| `recipients[]` | array<object> |  |
| `signature[]` | string |  |
| `subject[]` | string |  |
| `text[]` | string |  |
| `type[]` | string |  |
| `version[]` | string |  |

## Native endpoint

Through the native Front API, this operation is `GET /conversations/:conversation_id/messages` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conversation-messages.md) for the provider-specific parameters and requirements.

