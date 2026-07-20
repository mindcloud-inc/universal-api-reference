# Nimble: List Deal Pipelines

Retrieves available deal pipelines from Nimble.

```
GET https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-deal-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nimble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-deal-pipelines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-deal-pipelines?${params}`, {
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
      "defaultCurrency": "string",
      "description": {},
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
      "tabs": [
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
| `defaultCurrency` | string |  |
| `description` | object |  |
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
| `stages[].defaultProbability` | number |  |
| `stages[].description` | string |  |
| `stages[].expectedDays` | number |  |
| `stages[].name` | string |  |
| `stages[].pipelineId` | string |  |
| `stages[].role` | object |  |
| `stages[].role.isFinal` | boolean |  |
| `stages[].role.name` | string |  |
| `stages[].stageId` | string |  |
| `stages[].updated` | string |  |
| `tabs[]` | array<object> |  |
| `tabs[].members[]` | array<object> |  |
| `tabs[].members[].fields[]` | array<object> |  |
| `tabs[].members[].fields[].field` | object |  |
| `tabs[].members[].fields[].field.availableActions` | string |  |
| `tabs[].members[].fields[].field.fieldId` | string |  |
| `tabs[].members[].fields[].field.fieldName` | string |  |
| `tabs[].members[].fields[].field.fieldType` | object |  |
| `tabs[].members[].fields[].field.fieldType.fieldKind` | string |  |
| `tabs[].members[].fields[].field.fieldType.validationRule` | object |  |
| `tabs[].members[].fields[].field.modifier` | string |  |
| `tabs[].members[].fields[].field.multiples` | boolean |  |
| `tabs[].members[].fields[].type` | string |  |
| `tabs[].members[].groupId` | string |  |
| `tabs[].members[].groupName` | string |  |
| `tabs[].members[].logoId` | string |  |
| `tabs[].members[].type` | string |  |
| `tabs[].pipelineId` | string |  |
| `tabs[].tabId` | string |  |
| `tabs[].tabName` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Nimble API, this operation is `GET /api/v2/deals/pipelines` (base URL `https://app.nimble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deal-pipelines.md) for the provider-specific parameters and requirements.

