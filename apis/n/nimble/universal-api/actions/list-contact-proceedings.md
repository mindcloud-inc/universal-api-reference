# Nimble: List Contact Proceedings

Retrieves proceedings for a contact from Nimble.

```
GET https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contact-proceedings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nimble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contact-proceedings?connectionId=$CONNECTION_ID&contactId=69bc53298dd409a6ff02ab67&direction=past&limit=5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "69bc53298dd409a6ff02ab67",
  "direction": "past",
  "limit": "5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contact-proceedings?${params}`, {
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
| `contactId` | string | yes | Nimble contact_id path parameter. Example: `69bc53298dd409a6ff02ab67`. |
| `direction` | string | yes | Example: `past`. |
| `limit` | number | yes | Example: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "details": {
        "activityId": "string",
        "activityType": {
          "archived": true,
          "canUpdateDefinition": true,
          "canUpdateLc": true,
          "isCustom": true,
          "logoId": "string",
          "typeId": "string",
          "typeName": "Ava Chen"
        },
        "assignedTo": {
          "avatarUrl": {},
          "email": "ava@example.com",
          "isActive": true,
          "name": "Ava Chen",
          "userId": "string"
        },
        "comments": [
          [
            "string"
          ]
        ],
        "completedTstamp": "string",
        "created": "string",
        "description": "string",
        "details": {
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
            "69bc532677d905125927a64d": [
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
            ],
            "69bc532e8dd409a6ff02abc3": [
              [
                {}
              ]
            ],
            "69bc532e8dd409a6ff02abc4": [
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
            "actualCloseDate": [
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
            "quantity": [
              [
                {}
              ]
            ],
            "type": [
              [
                {}
              ]
            ],
            "wireStatus": [
              [
                {}
              ]
            ]
          },
          "files": [
            [
              "string"
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
            "expectedDays": {},
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
            "beforeFinalStage": {
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
            "string"
          ],
          "updated": "string",
          "updatedBy": {
            "avatarUrl": {},
            "email": "ava@example.com",
            "isActive": true,
            "name": "Ava Chen",
            "userId": "string"
          }
        },
        "feedTstamp": "string",
        "isImportant": {},
        "name": "Ava Chen",
        "newRelatedDeals": [
          [
            "string"
          ]
        ],
        "owner": {
          "avatarUrl": {},
          "email": "ava@example.com",
          "isActive": true,
          "name": "Ava Chen",
          "userId": "string"
        },
        "priority": {},
        "relatedContacts": [
          [
            {}
          ]
        ],
        "relatedDeals": [
          [
            "string"
          ]
        ],
        "scheduledTstamp": {},
        "tags": [
          [
            "string"
          ]
        ]
      },
      "feedTstamp": "string",
      "name": "Ava Chen",
      "proceedingId": "string",
      "proceedingType": {
        "typeId": "string",
        "typeName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `details` | object |  |
| `details.activityId` | string |  |
| `details.activityType` | object |  |
| `details.activityType.archived` | boolean |  |
| `details.activityType.canUpdateDefinition` | boolean |  |
| `details.activityType.canUpdateLc` | boolean |  |
| `details.activityType.isCustom` | boolean |  |
| `details.activityType.logoId` | string |  |
| `details.activityType.typeId` | string |  |
| `details.activityType.typeName` | string |  |
| `details.assignedTo` | object |  |
| `details.assignedTo.avatarUrl` | object |  |
| `details.assignedTo.email` | string |  |
| `details.assignedTo.isActive` | boolean |  |
| `details.assignedTo.name` | string |  |
| `details.assignedTo.userId` | string |  |
| `details.comments[]` | array<string> |  |
| `details.completedTstamp` | string |  |
| `details.created` | string |  |
| `details.description` | string |  |
| `details.details` | object |  |
| `details.details.ageInDays` | number |  |
| `details.details.created` | string |  |
| `details.details.creator` | object |  |
| `details.details.creator.avatarUrl` | object |  |
| `details.details.creator.email` | string |  |
| `details.details.creator.isActive` | boolean |  |
| `details.details.creator.name` | string |  |
| `details.details.creator.userId` | string |  |
| `details.details.currency` | string |  |
| `details.details.dealId` | string |  |
| `details.details.dealNumber` | number |  |
| `details.details.fieldsValues` | object |  |
| `details.details.fieldsValues.69bc532677d905125927a649[]` | array<object> |  |
| `details.details.fieldsValues.69bc532677d905125927a649[].isPrimary` | boolean |  |
| `details.details.fieldsValues.69bc532677d905125927a649[].value` | string |  |
| `details.details.fieldsValues.69bc532677d905125927a64a[]` | array<object> |  |
| `details.details.fieldsValues.69bc532677d905125927a64a[].isPrimary` | boolean |  |
| `details.details.fieldsValues.69bc532677d905125927a64a[].value` | string |  |
| `details.details.fieldsValues.69bc532677d905125927a64b[]` | array<object> |  |
| `details.details.fieldsValues.69bc532677d905125927a64b[].isPrimary` | boolean |  |
| `details.details.fieldsValues.69bc532677d905125927a64b[].value` | string |  |
| `details.details.fieldsValues.69bc532677d905125927a64d[]` | array<object> |  |
| `details.details.fieldsValues.69bc532677d905125927a64d[].isPrimary` | boolean |  |
| `details.details.fieldsValues.69bc532677d905125927a64d[].value` | string |  |
| `details.details.fieldsValues.69bc532677d905125927a64e[]` | array<object> |  |
| `details.details.fieldsValues.69bc532677d905125927a64e[].isPrimary` | boolean |  |
| `details.details.fieldsValues.69bc532677d905125927a64e[].value` | string |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02aba3[]` | array<object> |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02aba3[].isPrimary` | boolean |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02aba3[].value` | string |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02aba4[]` | array<object> |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02aba4[].isPrimary` | boolean |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02aba4[].value` | string |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02aba6[]` | array<object> |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02aba6[].isPrimary` | boolean |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02aba6[].value` | string |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02abc3[]` | array<object> |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02abc3[].isPrimary` | boolean |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02abc3[].value` | string |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02abc4[]` | array<object> |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02abc4[].isPrimary` | boolean |  |
| `details.details.fieldsValues.69bc532e8dd409a6ff02abc4[].value` | string |  |
| `details.details.fieldsValuesWithNames` | object |  |
| `details.details.fieldsValuesWithNames.3HolePunched[]` | array<object> |  |
| `details.details.fieldsValuesWithNames.3HolePunched[].isPrimary` | boolean |  |
| `details.details.fieldsValuesWithNames.3HolePunched[].value` | string |  |
| `details.details.fieldsValuesWithNames.actualCloseDate[]` | array<object> |  |
| `details.details.fieldsValuesWithNames.actualCloseDate[].isPrimary` | boolean |  |
| `details.details.fieldsValuesWithNames.actualCloseDate[].value` | string |  |
| `details.details.fieldsValuesWithNames.amount[]` | array<object> |  |
| `details.details.fieldsValuesWithNames.amount[].isPrimary` | boolean |  |
| `details.details.fieldsValuesWithNames.amount[].value` | string |  |
| `details.details.fieldsValuesWithNames.boxes[]` | array<object> |  |
| `details.details.fieldsValuesWithNames.boxes[].isPrimary` | boolean |  |
| `details.details.fieldsValuesWithNames.boxes[].value` | string |  |
| `details.details.fieldsValuesWithNames.description[]` | array<object> |  |
| `details.details.fieldsValuesWithNames.description[].isPrimary` | boolean |  |
| `details.details.fieldsValuesWithNames.description[].value` | string |  |
| `details.details.fieldsValuesWithNames.name[]` | array<object> |  |
| `details.details.fieldsValuesWithNames.name[].isPrimary` | boolean |  |
| `details.details.fieldsValuesWithNames.name[].value` | string |  |
| `details.details.fieldsValuesWithNames.probability[]` | array<object> |  |
| `details.details.fieldsValuesWithNames.probability[].isPrimary` | boolean |  |
| `details.details.fieldsValuesWithNames.probability[].value` | string |  |
| `details.details.fieldsValuesWithNames.quantity[]` | array<object> |  |
| `details.details.fieldsValuesWithNames.quantity[].isPrimary` | boolean |  |
| `details.details.fieldsValuesWithNames.quantity[].value` | string |  |
| `details.details.fieldsValuesWithNames.type[]` | array<object> |  |
| `details.details.fieldsValuesWithNames.type[].isPrimary` | boolean |  |
| `details.details.fieldsValuesWithNames.type[].value` | string |  |
| `details.details.fieldsValuesWithNames.wireStatus[]` | array<object> |  |
| `details.details.fieldsValuesWithNames.wireStatus[].isPrimary` | boolean |  |
| `details.details.fieldsValuesWithNames.wireStatus[].value` | string |  |
| `details.details.files[]` | array<string> |  |
| `details.details.finalProbability` | number |  |
| `details.details.isEditable` | boolean |  |
| `details.details.owner` | object |  |
| `details.details.owner.avatarUrl` | object |  |
| `details.details.owner.email` | string |  |
| `details.details.owner.isActive` | boolean |  |
| `details.details.owner.name` | string |  |
| `details.details.owner.userId` | string |  |
| `details.details.pipelineName` | string |  |
| `details.details.privacy` | object |  |
| `details.details.privacy.edit` | object |  |
| `details.details.privacy.edit.groupIds[]` | array<string> |  |
| `details.details.privacy.edit.userIds[]` | array<string> |  |
| `details.details.privacy.read` | object |  |
| `details.details.privacy.read.groupIds[]` | array<string> |  |
| `details.details.privacy.read.userIds[]` | array<string> |  |
| `details.details.relatedContacts[]` | array<object> |  |
| `details.details.relatedContacts[].contact` | object |  |
| `details.details.relatedContacts[].contact.avatarUrl` | string |  |
| `details.details.relatedContacts[].contact.contactType` | string |  |
| `details.details.relatedContacts[].contact.email[]` | string |  |
| `details.details.relatedContacts[].contact.employment` | object |  |
| `details.details.relatedContacts[].contact.employment.companyName` | string |  |
| `details.details.relatedContacts[].contact.employment.title` | string |  |
| `details.details.relatedContacts[].contact.id` | string |  |
| `details.details.relatedContacts[].contact.isViewable` | boolean |  |
| `details.details.relatedContacts[].contact.name` | string |  |
| `details.details.relatedContacts[].contact.phones[]` | array<string> |  |
| `details.details.relatedContacts[].contact.subtitle` | string |  |
| `details.details.relatedContacts[].contact.title` | string |  |
| `details.details.relatedContacts[].employments[]` | array<object> |  |
| `details.details.relatedContacts[].employments[].employer` | object |  |
| `details.details.relatedContacts[].employments[].employer.avatarUrl` | string |  |
| `details.details.relatedContacts[].employments[].employer.contactType` | string |  |
| `details.details.relatedContacts[].employments[].employer.email[]` | array<string> |  |
| `details.details.relatedContacts[].employments[].employer.employment` | object |  |
| `details.details.relatedContacts[].employments[].employer.id` | string |  |
| `details.details.relatedContacts[].employments[].employer.isViewable` | boolean |  |
| `details.details.relatedContacts[].employments[].employer.name` | string |  |
| `details.details.relatedContacts[].employments[].employer.phones[]` | array<string> |  |
| `details.details.relatedContacts[].employments[].employer.subtitle` | object |  |
| `details.details.relatedContacts[].employments[].employer.title` | object |  |
| `details.details.relatedContacts[].employments[].endDate` | object |  |
| `details.details.relatedContacts[].employments[].startDate` | string |  |
| `details.details.relatedContacts[].employments[].title` | string |  |
| `details.details.relatedContacts[].note` | object |  |
| `details.details.relatedExternalContacts[]` | array<string> |  |
| `details.details.stage` | object |  |
| `details.details.stage.archivedAt` | object |  |
| `details.details.stage.created` | string |  |
| `details.details.stage.creator` | object |  |
| `details.details.stage.creator.avatarUrl` | object |  |
| `details.details.stage.creator.email` | string |  |
| `details.details.stage.creator.isActive` | boolean |  |
| `details.details.stage.creator.name` | string |  |
| `details.details.stage.creator.userId` | string |  |
| `details.details.stage.defaultProbability` | number |  |
| `details.details.stage.description` | string |  |
| `details.details.stage.expectedDays` | object |  |
| `details.details.stage.name` | string |  |
| `details.details.stage.pipelineId` | string |  |
| `details.details.stage.role` | object |  |
| `details.details.stage.role.isFinal` | boolean |  |
| `details.details.stage.role.name` | string |  |
| `details.details.stage.stageId` | string |  |
| `details.details.stage.updated` | string |  |
| `details.details.stageTransitions` | object |  |
| `details.details.stageTransitions.beforeFinalStage` | object |  |
| `details.details.stageTransitions.beforeFinalStage.archivedAt` | object |  |
| `details.details.stageTransitions.beforeFinalStage.created` | string |  |
| `details.details.stageTransitions.beforeFinalStage.creator` | object |  |
| `details.details.stageTransitions.beforeFinalStage.creator.avatarUrl` | object |  |
| `details.details.stageTransitions.beforeFinalStage.creator.email` | string |  |
| `details.details.stageTransitions.beforeFinalStage.creator.isActive` | boolean |  |
| `details.details.stageTransitions.beforeFinalStage.creator.name` | string |  |
| `details.details.stageTransitions.beforeFinalStage.creator.userId` | string |  |
| `details.details.stageTransitions.beforeFinalStage.defaultProbability` | number |  |
| `details.details.stageTransitions.beforeFinalStage.description` | string |  |
| `details.details.stageTransitions.beforeFinalStage.expectedDays` | number |  |
| `details.details.stageTransitions.beforeFinalStage.name` | string |  |
| `details.details.stageTransitions.beforeFinalStage.pipelineId` | string |  |
| `details.details.stageTransitions.beforeFinalStage.role` | object |  |
| `details.details.stageTransitions.beforeFinalStage.role.isFinal` | boolean |  |
| `details.details.stageTransitions.beforeFinalStage.role.name` | string |  |
| `details.details.stageTransitions.beforeFinalStage.stageId` | string |  |
| `details.details.stageTransitions.beforeFinalStage.updated` | string |  |
| `details.details.stageTransitions.lastEnteredDate` | string |  |
| `details.details.stageTransitions.pipelineColor` | string |  |
| `details.details.stageTransitions.pipelineId` | string |  |
| `details.details.stageTransitions.pipelineName` | string |  |
| `details.details.stageTransitions.transitions[]` | array<object> |  |
| `details.details.stageTransitions.transitions[].fromStage` | object |  |
| `details.details.stageTransitions.transitions[].lostReason` | object |  |
| `details.details.stageTransitions.transitions[].notes` | object |  |
| `details.details.stageTransitions.transitions[].toStage` | object |  |
| `details.details.stageTransitions.transitions[].toStage.archivedAt` | object |  |
| `details.details.stageTransitions.transitions[].toStage.created` | string |  |
| `details.details.stageTransitions.transitions[].toStage.creator` | object |  |
| `details.details.stageTransitions.transitions[].toStage.creator.avatarUrl` | object |  |
| `details.details.stageTransitions.transitions[].toStage.creator.email` | string |  |
| `details.details.stageTransitions.transitions[].toStage.creator.isActive` | boolean |  |
| `details.details.stageTransitions.transitions[].toStage.creator.name` | string |  |
| `details.details.stageTransitions.transitions[].toStage.creator.userId` | string |  |
| `details.details.stageTransitions.transitions[].toStage.defaultProbability` | number |  |
| `details.details.stageTransitions.transitions[].toStage.description` | string |  |
| `details.details.stageTransitions.transitions[].toStage.expectedDays` | number |  |
| `details.details.stageTransitions.transitions[].toStage.name` | string |  |
| `details.details.stageTransitions.transitions[].toStage.pipelineId` | string |  |
| `details.details.stageTransitions.transitions[].toStage.role` | object |  |
| `details.details.stageTransitions.transitions[].toStage.role.isFinal` | boolean |  |
| `details.details.stageTransitions.transitions[].toStage.role.name` | string |  |
| `details.details.stageTransitions.transitions[].toStage.stageId` | string |  |
| `details.details.stageTransitions.transitions[].toStage.updated` | string |  |
| `details.details.stageTransitions.transitions[].when` | string |  |
| `details.details.stageTransitions.transitions[].who` | object |  |
| `details.details.stageTransitions.transitions[].who.avatarUrl` | object |  |
| `details.details.stageTransitions.transitions[].who.email` | string |  |
| `details.details.stageTransitions.transitions[].who.isActive` | boolean |  |
| `details.details.stageTransitions.transitions[].who.name` | string |  |
| `details.details.stageTransitions.transitions[].who.userId` | string |  |
| `details.details.tags[]` | string |  |
| `details.details.updated` | string |  |
| `details.details.updatedBy` | object |  |
| `details.details.updatedBy.avatarUrl` | object |  |
| `details.details.updatedBy.email` | string |  |
| `details.details.updatedBy.isActive` | boolean |  |
| `details.details.updatedBy.name` | string |  |
| `details.details.updatedBy.userId` | string |  |
| `details.feedTstamp` | string |  |
| `details.isImportant` | object |  |
| `details.name` | string |  |
| `details.newRelatedDeals[]` | array<string> |  |
| `details.owner` | object |  |
| `details.owner.avatarUrl` | object |  |
| `details.owner.email` | string |  |
| `details.owner.isActive` | boolean |  |
| `details.owner.name` | string |  |
| `details.owner.userId` | string |  |
| `details.priority` | object |  |
| `details.relatedContacts[]` | array<object> |  |
| `details.relatedContacts[].avatarUrl` | string |  |
| `details.relatedContacts[].contactType` | string |  |
| `details.relatedContacts[].email[]` | string |  |
| `details.relatedContacts[].employment` | object |  |
| `details.relatedContacts[].employment.companyName` | string |  |
| `details.relatedContacts[].employment.title` | string |  |
| `details.relatedContacts[].id` | string |  |
| `details.relatedContacts[].isViewable` | boolean |  |
| `details.relatedContacts[].name` | string |  |
| `details.relatedContacts[].phones[]` | array<string> |  |
| `details.relatedContacts[].subtitle` | string |  |
| `details.relatedContacts[].title` | string |  |
| `details.relatedDeals[]` | array<string> |  |
| `details.scheduledTstamp` | object |  |
| `details.tags[]` | array<string> |  |
| `feedTstamp` | string |  |
| `name` | string |  |
| `proceedingId` | string |  |
| `proceedingType` | object |  |
| `proceedingType.typeId` | string |  |
| `proceedingType.typeName` | string |  |

## Native endpoint

Through the native Nimble API, this operation is `GET /api/v1/contacts/:contact_id/proceedings` (base URL `https://app.nimble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-proceedings.md) for the provider-specific parameters and requirements.

