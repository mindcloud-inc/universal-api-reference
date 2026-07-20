# Nimble: Create Draft Message

Creates a draft message in Nimble.

```
POST https://connect.mindcloud.co/v1/universal/nimble/latest/actions/create-draft-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nimble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/create-draft-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nimble/latest/actions/create-draft-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipients[]` | array<object> | no |  |
| `subject` | string | no |  |
| `body` | string | no |  |
| `senderCredentialId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bcc": [
        [
          {}
        ]
      ],
      "cc": [
        [
          {}
        ]
      ],
      "creator": {
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "isActive": true,
        "name": "Ava Chen",
        "userId": "string"
      },
      "draftId": "string",
      "recipients": [
        [
          {}
        ]
      ],
      "specification": {
        "attachments": [
          [
            {}
          ]
        ],
        "bcc": [
          [
            {}
          ]
        ],
        "body": "string",
        "cc": [
          [
            {}
          ]
        ],
        "recipients": [
          [
            {}
          ]
        ],
        "senderCredentialId": "string",
        "subject": "string",
        "trackingConfiguration": {
          "clicksTracking": true,
          "opensTracking": true
        },
        "trackingEnabled": true
      },
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bcc[]` | array<object> |  |
| `cc[]` | array<object> |  |
| `creator` | object |  |
| `creator.avatarUrl` | string |  |
| `creator.email` | string |  |
| `creator.isActive` | boolean |  |
| `creator.name` | string |  |
| `creator.userId` | string |  |
| `draftId` | string |  |
| `recipients[]` | array<object> |  |
| `specification` | object |  |
| `specification.attachments[]` | array<object> |  |
| `specification.bcc[]` | array<object> |  |
| `specification.body` | string |  |
| `specification.cc[]` | array<object> |  |
| `specification.recipients[]` | array<object> |  |
| `specification.senderCredentialId` | string |  |
| `specification.subject` | string |  |
| `specification.trackingConfiguration` | object |  |
| `specification.trackingConfiguration.clicksTracking` | boolean |  |
| `specification.trackingConfiguration.opensTracking` | boolean |  |
| `specification.trackingEnabled` | boolean |  |
| `updated` | string |  |

## Native endpoint

Through the native Nimble API, this operation is `POST /api/v1/messages/drafts` (base URL `https://app.nimble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-message.md) for the provider-specific parameters and requirements.

