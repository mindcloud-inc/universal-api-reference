# Nimble: Create Deal

Creates a new deal in Nimble.

```
POST https://connect.mindcloud.co/v1/universal/nimble/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nimble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pipelineId": "string",
  "stageId": "string",
  "fieldsValues": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nimble/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pipelineId": "string",
    "stageId": "string",
    "fieldsValues": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pipelineId` | string | yes |  |
| `stageId` | string | yes |  |
| `fieldsValues` | object | yes |  |
| `tags[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ageInDays": 1,
      "created": "string",
      "creator": {
        "avatarUrl": {},
        "email": "ava@example.com",
        "isActive": true,
        "name": "Ava Chen",
        "userId": "string"
      },
      "currency": "string",
      "dealId": "string",
      "dealNumber": 1,
      "fieldsValues": {
        "69bc532677d905125927a649": [
          [
            {}
          ]
        ],
        "69bc532677d905125927a64a": [
          [
            {}
          ]
        ],
        "69bc532677d905125927a64b": [
          [
            {}
          ]
        ],
        "69bc532677d905125927a64c": [
          [
            {}
          ]
        ],
        "69bc532677d905125927a64e": [
          [
            {}
          ]
        ],
        "69bc532e8dd409a6ff02aba3": [
          [
            {}
          ]
        ],
        "69bc532e8dd409a6ff02aba4": [
          [
            {}
          ]
        ],
        "69bc532e8dd409a6ff02aba6": [
          [
            {}
          ]
        ]
      },
      "fieldsValuesWithNames": {
        "3HolePunched": [
          [
            {}
          ]
        ],
        "amount": [
          [
            {}
          ]
        ],
        "boxes": [
          [
            {}
          ]
        ],
        "description": [
          [
            {}
          ]
        ],
        "expectedCloseDate": [
          [
            {}
          ]
        ],
        "name": [
          [
            {}
          ]
        ],
        "probability": [
          [
            {}
          ]
        ],
        "type": [
          [
            {}
          ]
        ]
      },
      "files": [
        [
          {}
        ]
      ],
      "finalProbability": 1,
      "isEditable": true,
      "owner": {
        "avatarUrl": {},
        "email": "ava@example.com",
        "isActive": true,
        "name": "Ava Chen",
        "userId": "string"
      },
      "pipelineName": "Ava Chen",
      "privacy": {
        "edit": {
          "groupIds": [
            [
              "string"
            ]
          ],
          "userIds": [
            [
              "string"
            ]
          ]
        },
        "read": {
          "groupIds": [
            [
              "string"
            ]
          ],
          "userIds": [
            [
              "string"
            ]
          ]
        }
      },
      "relatedContacts": [
        [
          {}
        ]
      ],
      "relatedExternalContacts": [
        [
          "string"
        ]
      ],
      "stage": {
        "archivedAt": {},
        "created": "string",
        "creator": {
          "avatarUrl": {},
          "email": "ava@example.com",
          "isActive": true,
          "name": "Ava Chen",
          "userId": "string"
        },
        "defaultProbability": 1,
        "description": "string",
        "expectedDays": 1,
        "name": "Ava Chen",
        "pipelineId": "string",
        "role": {
          "isFinal": true,
          "name": "Ava Chen"
        },
        "stageId": "string",
        "updated": "string"
      },
      "stageTransitions": {
        "beforeFinalStage": {},
        "lastEnteredDate": "string",
        "pipelineColor": "string",
        "pipelineId": "string",
        "pipelineName": "Ava Chen",
        "transitions": [
          [
            {}
          ]
        ]
      },
      "tags": [
        [
          "string"
        ]
      ],
      "updated": "string",
      "updatedBy": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ageInDays` | number |  |
| `created` | string |  |
| `creator` | object |  |
| `creator.avatarUrl` | object |  |
| `creator.email` | string |  |
| `creator.isActive` | boolean |  |
| `creator.name` | string |  |
| `creator.userId` | string |  |
| `currency` | string |  |
| `dealId` | string |  |
| `dealNumber` | number |  |
| `fieldsValues` | object |  |
| `fieldsValues.69bc532677d905125927a649[]` | array<object> |  |
| `fieldsValues.69bc532677d905125927a649[].isPrimary` | boolean |  |
| `fieldsValues.69bc532677d905125927a649[].value` | string |  |
| `fieldsValues.69bc532677d905125927a64a[]` | array<object> |  |
| `fieldsValues.69bc532677d905125927a64a[].isPrimary` | boolean |  |
| `fieldsValues.69bc532677d905125927a64a[].value` | string |  |
| `fieldsValues.69bc532677d905125927a64b[]` | array<object> |  |
| `fieldsValues.69bc532677d905125927a64b[].isPrimary` | boolean |  |
| `fieldsValues.69bc532677d905125927a64b[].value` | string |  |
| `fieldsValues.69bc532677d905125927a64c[]` | array<object> |  |
| `fieldsValues.69bc532677d905125927a64c[].isPrimary` | boolean |  |
| `fieldsValues.69bc532677d905125927a64c[].value` | string |  |
| `fieldsValues.69bc532677d905125927a64e[]` | array<object> |  |
| `fieldsValues.69bc532677d905125927a64e[].isPrimary` | boolean |  |
| `fieldsValues.69bc532677d905125927a64e[].value` | string |  |
| `fieldsValues.69bc532e8dd409a6ff02aba3[]` | array<object> |  |
| `fieldsValues.69bc532e8dd409a6ff02aba3[].isPrimary` | boolean |  |
| `fieldsValues.69bc532e8dd409a6ff02aba3[].value` | string |  |
| `fieldsValues.69bc532e8dd409a6ff02aba4[]` | array<object> |  |
| `fieldsValues.69bc532e8dd409a6ff02aba4[].isPrimary` | boolean |  |
| `fieldsValues.69bc532e8dd409a6ff02aba4[].value` | string |  |
| `fieldsValues.69bc532e8dd409a6ff02aba6[]` | array<object> |  |
| `fieldsValues.69bc532e8dd409a6ff02aba6[].isPrimary` | boolean |  |
| `fieldsValues.69bc532e8dd409a6ff02aba6[].value` | string |  |
| `fieldsValuesWithNames` | object |  |
| `fieldsValuesWithNames.3HolePunched[]` | array<object> |  |
| `fieldsValuesWithNames.3HolePunched[].isPrimary` | boolean |  |
| `fieldsValuesWithNames.3HolePunched[].value` | string |  |
| `fieldsValuesWithNames.amount[]` | array<object> |  |
| `fieldsValuesWithNames.amount[].isPrimary` | boolean |  |
| `fieldsValuesWithNames.amount[].value` | string |  |
| `fieldsValuesWithNames.boxes[]` | array<object> |  |
| `fieldsValuesWithNames.boxes[].isPrimary` | boolean |  |
| `fieldsValuesWithNames.boxes[].value` | string |  |
| `fieldsValuesWithNames.description[]` | array<object> |  |
| `fieldsValuesWithNames.description[].isPrimary` | boolean |  |
| `fieldsValuesWithNames.description[].value` | string |  |
| `fieldsValuesWithNames.expectedCloseDate[]` | array<object> |  |
| `fieldsValuesWithNames.expectedCloseDate[].isPrimary` | boolean |  |
| `fieldsValuesWithNames.expectedCloseDate[].value` | string |  |
| `fieldsValuesWithNames.name[]` | array<object> |  |
| `fieldsValuesWithNames.name[].isPrimary` | boolean |  |
| `fieldsValuesWithNames.name[].value` | string |  |
| `fieldsValuesWithNames.probability[]` | array<object> |  |
| `fieldsValuesWithNames.probability[].isPrimary` | boolean |  |
| `fieldsValuesWithNames.probability[].value` | string |  |
| `fieldsValuesWithNames.type[]` | array<object> |  |
| `fieldsValuesWithNames.type[].isPrimary` | boolean |  |
| `fieldsValuesWithNames.type[].value` | string |  |
| `files[]` | array<object> |  |
| `files[].fileId` | string |  |
| `files[].fileName` | string |  |
| `files[].fileSize` | number |  |
| `files[].metadata` | object |  |
| `files[].metadata.fileUrl` | string |  |
| `files[].metadata.iconUrl` | object |  |
| `files[].metadata.source` | string |  |
| `files[].mimeType` | string |  |
| `files[].uploadedAt` | string |  |
| `files[].uploader` | object |  |
| `files[].uploader.avatarUrl` | object |  |
| `files[].uploader.email` | string |  |
| `files[].uploader.isActive` | boolean |  |
| `files[].uploader.name` | string |  |
| `files[].uploader.userId` | string |  |
| `finalProbability` | number |  |
| `isEditable` | boolean |  |
| `owner` | object |  |
| `owner.avatarUrl` | object |  |
| `owner.email` | string |  |
| `owner.isActive` | boolean |  |
| `owner.name` | string |  |
| `owner.userId` | string |  |
| `pipelineName` | string |  |
| `privacy` | object |  |
| `privacy.edit` | object |  |
| `privacy.edit.groupIds[]` | array<string> |  |
| `privacy.edit.userIds[]` | array<string> |  |
| `privacy.read` | object |  |
| `privacy.read.groupIds[]` | array<string> |  |
| `privacy.read.userIds[]` | array<string> |  |
| `relatedContacts[]` | array<object> |  |
| `relatedContacts[].contact` | object |  |
| `relatedContacts[].contact.avatarUrl` | string |  |
| `relatedContacts[].contact.contactType` | string |  |
| `relatedContacts[].contact.email[]` | array<string> |  |
| `relatedContacts[].contact.employment` | object |  |
| `relatedContacts[].contact.employment.companyName` | object |  |
| `relatedContacts[].contact.employment.title` | string |  |
| `relatedContacts[].contact.id` | string |  |
| `relatedContacts[].contact.isViewable` | boolean |  |
| `relatedContacts[].contact.name` | string |  |
| `relatedContacts[].contact.phones[]` | array<string> |  |
| `relatedContacts[].contact.subtitle` | string |  |
| `relatedContacts[].contact.title` | string |  |
| `relatedContacts[].employments[]` | array<string> |  |
| `relatedContacts[].note` | object |  |
| `relatedExternalContacts[]` | array<string> |  |
| `stage` | object |  |
| `stage.archivedAt` | object |  |
| `stage.created` | string |  |
| `stage.creator` | object |  |
| `stage.creator.avatarUrl` | object |  |
| `stage.creator.email` | string |  |
| `stage.creator.isActive` | boolean |  |
| `stage.creator.name` | string |  |
| `stage.creator.userId` | string |  |
| `stage.defaultProbability` | number |  |
| `stage.description` | string |  |
| `stage.expectedDays` | number |  |
| `stage.name` | string |  |
| `stage.pipelineId` | string |  |
| `stage.role` | object |  |
| `stage.role.isFinal` | boolean |  |
| `stage.role.name` | string |  |
| `stage.stageId` | string |  |
| `stage.updated` | string |  |
| `stageTransitions` | object |  |
| `stageTransitions.beforeFinalStage` | object |  |
| `stageTransitions.lastEnteredDate` | string |  |
| `stageTransitions.pipelineColor` | string |  |
| `stageTransitions.pipelineId` | string |  |
| `stageTransitions.pipelineName` | string |  |
| `stageTransitions.transitions[]` | array<object> |  |
| `stageTransitions.transitions[].fromStage` | object |  |
| `stageTransitions.transitions[].lostReason` | object |  |
| `stageTransitions.transitions[].notes` | object |  |
| `stageTransitions.transitions[].toStage` | object |  |
| `stageTransitions.transitions[].toStage.archivedAt` | object |  |
| `stageTransitions.transitions[].toStage.created` | string |  |
| `stageTransitions.transitions[].toStage.creator` | object |  |
| `stageTransitions.transitions[].toStage.creator.avatarUrl` | object |  |
| `stageTransitions.transitions[].toStage.creator.email` | string |  |
| `stageTransitions.transitions[].toStage.creator.isActive` | boolean |  |
| `stageTransitions.transitions[].toStage.creator.name` | string |  |
| `stageTransitions.transitions[].toStage.creator.userId` | string |  |
| `stageTransitions.transitions[].toStage.defaultProbability` | number |  |
| `stageTransitions.transitions[].toStage.description` | string |  |
| `stageTransitions.transitions[].toStage.expectedDays` | number |  |
| `stageTransitions.transitions[].toStage.name` | string |  |
| `stageTransitions.transitions[].toStage.pipelineId` | string |  |
| `stageTransitions.transitions[].toStage.role` | object |  |
| `stageTransitions.transitions[].toStage.role.isFinal` | boolean |  |
| `stageTransitions.transitions[].toStage.role.name` | string |  |
| `stageTransitions.transitions[].toStage.stageId` | string |  |
| `stageTransitions.transitions[].toStage.updated` | string |  |
| `stageTransitions.transitions[].when` | string |  |
| `stageTransitions.transitions[].who` | object |  |
| `stageTransitions.transitions[].who.avatarUrl` | object |  |
| `stageTransitions.transitions[].who.email` | string |  |
| `stageTransitions.transitions[].who.isActive` | boolean |  |
| `stageTransitions.transitions[].who.name` | string |  |
| `stageTransitions.transitions[].who.userId` | string |  |
| `tags[]` | array<string> |  |
| `updated` | string |  |
| `updatedBy` | object |  |

## Native endpoint

Through the native Nimble API, this operation is `POST /api/v2/deals` (base URL `https://app.nimble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

