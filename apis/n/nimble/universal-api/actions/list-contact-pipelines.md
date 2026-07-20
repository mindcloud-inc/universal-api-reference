# Nimble: List Contact Pipelines

Retrieves available contact pipelines from Nimble.

```
GET https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contact-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nimble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contact-pipelines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contact-pipelines?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": {},
      "color": "string",
      "created": "string",
      "creator": {
        "avatarUrl": {},
        "email": "ava@example.com",
        "isActive": true,
        "name": "Ava Chen",
        "userId": "string"
      },
      "description": "string",
      "fields": [
        [
          "string"
        ]
      ],
      "isDefault": true,
      "lostReasons": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "pipelineId": "string",
      "stages": [
        [
          {}
        ]
      ],
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | object |  |
| `color` | string |  |
| `created` | string |  |
| `creator` | object |  |
| `creator.avatarUrl` | object |  |
| `creator.email` | string |  |
| `creator.isActive` | boolean |  |
| `creator.name` | string |  |
| `creator.userId` | string |  |
| `description` | string |  |
| `fields[]` | array<string> |  |
| `isDefault` | boolean |  |
| `lostReasons[]` | array<object> |  |
| `lostReasons[].id` | string |  |
| `lostReasons[].text` | string |  |
| `name` | string |  |
| `pipelineId` | string |  |
| `stages[]` | array<object> |  |
| `stages[].archivedAt` | object |  |
| `stages[].created` | string |  |
| `stages[].creator` | object |  |
| `stages[].creator.avatarUrl` | object |  |
| `stages[].creator.email` | string |  |
| `stages[].creator.isActive` | boolean |  |
| `stages[].creator.name` | string |  |
| `stages[].creator.userId` | string |  |
| `stages[].daysLimit` | object |  |
| `stages[].description` | string |  |
| `stages[].name` | string |  |
| `stages[].pipelineId` | string |  |
| `stages[].role` | object |  |
| `stages[].role.isFinal` | boolean |  |
| `stages[].role.name` | string |  |
| `stages[].stageId` | string |  |
| `stages[].updated` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Nimble API, this operation is `GET /api/v1/contacts/pipelines` (base URL `https://app.nimble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-pipelines.md) for the provider-specific parameters and requirements.

