# Awork: Search Workspace

Finds workspace entities in Awork by search term.

```
GET https://connect.mindcloud.co/v1/universal/awork/latest/actions/search-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/awork/latest/actions/search-workspace?connectionId=$CONNECTION_ID&searchTerm=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchTerm": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/awork/latest/actions/search-workspace?${params}`, {
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
| `searchTerm` | string | yes | Search text to match across the selected resource types. |
| `searchTypes` | string | no | Comma-separated resource types to search in awork. |
| `top` | number | no | Maximum number of search results to return. |
| `includeClosedAndStuck` | boolean | no | Whether to include closed and stuck entities in search results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentHits": {
        "hasHits": true,
        "hits": [
          {
            "entity": {
              "entityId": "string",
              "entityType": "string",
              "id": "string",
              "indexTime": "2026-05-07T12:00:00.000Z",
              "isExternal": true,
              "isHiddenForConnectUsers": true,
              "message": "string",
              "task": {
                "baseType": "string",
                "createdBy": "string",
                "id": "string",
                "isExternal": true,
                "isHiddenForConnectUsers": true,
                "name": "Ava Chen",
                "project": {
                  "createdBy": "string",
                  "id": "string",
                  "isExternal": true,
                  "isPrivate": true,
                  "members": [
                    {
                      "id": "string",
                      "projectRoleId": "string",
                      "userId": "string"
                    }
                  ],
                  "name": "Ava Chen"
                },
                "projectId": "string",
                "taskStatus": {
                  "name": "Ava Chen",
                  "type": "string"
                }
              },
              "userId": "string",
              "workspaceId": "string"
            },
            "highlights": {
              "task": {
                "name": [
                  "Ava Chen"
                ]
              }
            },
            "score": 1,
            "type": "string"
          }
        ],
        "maxScore": 1,
        "totalCount": 1
      },
      "companyHits": {
        "hasHits": true,
        "maxScore": 1,
        "totalCount": 1
      },
      "dashboardNotesHits": {
        "hasHits": true,
        "maxScore": 1,
        "totalCount": 1
      },
      "documentHits": {
        "hasHits": true,
        "hits": [
          {
            "entity": {
              "documentSpace": {
                "id": "string",
                "name": "Ava Chen",
                "workspaceAccessLevel": "string"
              },
              "documentSpaceId": "string",
              "emoji": "string",
              "id": "string",
              "indexTime": "2026-05-07T12:00:00.000Z",
              "isExternal": true,
              "isHiddenForConnectUsers": true,
              "isPrivate": true,
              "name": "Ava Chen",
              "rootDocumentCreatedBy": "string",
              "workspaceId": "string"
            },
            "highlights": {
              "content": [
                "string"
              ]
            },
            "score": 1,
            "type": "string"
          }
        ],
        "maxScore": 1,
        "totalCount": 1
      },
      "fileHits": {
        "hasHits": true,
        "maxScore": 1,
        "totalCount": 1
      },
      "maxScore": 1,
      "projectHits": {
        "hasHits": true,
        "maxScore": 1,
        "totalCount": 1
      },
      "taskHits": {
        "hasHits": true,
        "hits": [
          {
            "entity": {
              "baseType": "string",
              "correlationId": "string",
              "createdBy": "string",
              "description": "string",
              "id": "string",
              "indexTime": "2026-05-07T12:00:00.000Z",
              "isExternal": true,
              "isHiddenForConnectUsers": true,
              "isOpen": true,
              "isPrio": true,
              "lists": [
                "string"
              ],
              "name": "Ava Chen",
              "plannedDuration": 1,
              "project": {
                "createdBy": "string",
                "id": "string",
                "isBillableByDefault": true,
                "isExternal": true,
                "isPrivate": true,
                "members": [
                  {
                    "id": "string",
                    "projectRoleId": "string",
                    "projectRoleName": "Ava Chen",
                    "userId": "string"
                  }
                ],
                "name": "Ava Chen",
                "projectStatus": {
                  "id": "string",
                  "name": "Ava Chen",
                  "type": "string"
                }
              },
              "projectId": "string",
              "taskIdentifier": "string",
              "taskStatus": {
                "icon": "string",
                "name": "Ava Chen",
                "type": "string"
              },
              "typeOfWork": {
                "name": "Ava Chen"
              },
              "userStats": [
                {
                  "lastOpened": 1,
                  "openCount": 1,
                  "userId": "string"
                }
              ],
              "workspaceId": "string"
            },
            "highlights": {
              "name": [
                "Ava Chen"
              ]
            },
            "score": 1,
            "type": "string"
          }
        ],
        "maxScore": 1,
        "totalCount": 1
      },
      "taskListHits": {
        "hasHits": true,
        "maxScore": 1,
        "totalCount": 1
      },
      "timeEntriesHits": {
        "hasHits": true,
        "maxScore": 1,
        "totalCount": 1
      },
      "timeReportsHits": {
        "hasHits": true,
        "maxScore": 1,
        "totalCount": 1
      },
      "top": [
        {
          "entity": {
            "baseType": "string",
            "correlationId": "string",
            "createdBy": "string",
            "description": "string",
            "id": "string",
            "indexTime": "2026-05-07T12:00:00.000Z",
            "isExternal": true,
            "isHiddenForConnectUsers": true,
            "isOpen": true,
            "isPrio": true,
            "lists": [
              "string"
            ],
            "name": "Ava Chen",
            "plannedDuration": 1,
            "project": {
              "createdBy": "string",
              "id": "string",
              "isBillableByDefault": true,
              "isExternal": true,
              "isPrivate": true,
              "members": [
                {
                  "id": "string",
                  "projectRoleId": "string",
                  "projectRoleName": "Ava Chen",
                  "userId": "string"
                }
              ],
              "name": "Ava Chen",
              "projectStatus": {
                "id": "string",
                "name": "Ava Chen",
                "type": "string"
              }
            },
            "projectId": "string",
            "taskIdentifier": "string",
            "taskStatus": {
              "icon": "string",
              "name": "Ava Chen",
              "type": "string"
            },
            "typeOfWork": {
              "name": "Ava Chen"
            },
            "userStats": [
              {
                "lastOpened": 1,
                "openCount": 1,
                "userId": "string"
              }
            ],
            "workspaceId": "string"
          },
          "highlights": {
            "name": [
              "Ava Chen"
            ]
          },
          "score": 1,
          "type": "string"
        }
      ],
      "totalCount": 1,
      "userHits": {
        "hasHits": true,
        "maxScore": 1,
        "totalCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentHits.hasHits` | boolean |  |
| `commentHits.hits[].entity.entityId` | string |  |
| `commentHits.hits[].entity.entityType` | string |  |
| `commentHits.hits[].entity.id` | string |  |
| `commentHits.hits[].entity.indexTime` | date |  |
| `commentHits.hits[].entity.isExternal` | boolean |  |
| `commentHits.hits[].entity.isHiddenForConnectUsers` | boolean |  |
| `commentHits.hits[].entity.message` | string |  |
| `commentHits.hits[].entity.task.baseType` | string |  |
| `commentHits.hits[].entity.task.createdBy` | string |  |
| `commentHits.hits[].entity.task.id` | string |  |
| `commentHits.hits[].entity.task.isExternal` | boolean |  |
| `commentHits.hits[].entity.task.isHiddenForConnectUsers` | boolean |  |
| `commentHits.hits[].entity.task.name` | string |  |
| `commentHits.hits[].entity.task.project.createdBy` | string |  |
| `commentHits.hits[].entity.task.project.id` | string |  |
| `commentHits.hits[].entity.task.project.isExternal` | boolean |  |
| `commentHits.hits[].entity.task.project.isPrivate` | boolean |  |
| `commentHits.hits[].entity.task.project.members[].id` | string |  |
| `commentHits.hits[].entity.task.project.members[].projectRoleId` | string |  |
| `commentHits.hits[].entity.task.project.members[].userId` | string |  |
| `commentHits.hits[].entity.task.project.name` | string |  |
| `commentHits.hits[].entity.task.projectId` | string |  |
| `commentHits.hits[].entity.task.taskStatus.name` | string |  |
| `commentHits.hits[].entity.task.taskStatus.type` | string |  |
| `commentHits.hits[].entity.userId` | string |  |
| `commentHits.hits[].entity.workspaceId` | string |  |
| `commentHits.hits[].highlights.task.name[]` | string |  |
| `commentHits.hits[].score` | number |  |
| `commentHits.hits[].type` | string |  |
| `commentHits.maxScore` | number |  |
| `commentHits.totalCount` | number |  |
| `companyHits.hasHits` | boolean |  |
| `companyHits.maxScore` | number |  |
| `companyHits.totalCount` | number |  |
| `dashboardNotesHits.hasHits` | boolean |  |
| `dashboardNotesHits.maxScore` | number |  |
| `dashboardNotesHits.totalCount` | number |  |
| `documentHits.hasHits` | boolean |  |
| `documentHits.hits[].entity.documentSpace.id` | string |  |
| `documentHits.hits[].entity.documentSpace.name` | string |  |
| `documentHits.hits[].entity.documentSpace.workspaceAccessLevel` | string |  |
| `documentHits.hits[].entity.documentSpaceId` | string |  |
| `documentHits.hits[].entity.emoji` | string |  |
| `documentHits.hits[].entity.id` | string |  |
| `documentHits.hits[].entity.indexTime` | date |  |
| `documentHits.hits[].entity.isExternal` | boolean |  |
| `documentHits.hits[].entity.isHiddenForConnectUsers` | boolean |  |
| `documentHits.hits[].entity.isPrivate` | boolean |  |
| `documentHits.hits[].entity.name` | string |  |
| `documentHits.hits[].entity.rootDocumentCreatedBy` | string |  |
| `documentHits.hits[].entity.workspaceId` | string |  |
| `documentHits.hits[].highlights.content[]` | string |  |
| `documentHits.hits[].score` | number |  |
| `documentHits.hits[].type` | string |  |
| `documentHits.maxScore` | number |  |
| `documentHits.totalCount` | number |  |
| `fileHits.hasHits` | boolean |  |
| `fileHits.maxScore` | number |  |
| `fileHits.totalCount` | number |  |
| `maxScore` | number |  |
| `projectHits.hasHits` | boolean |  |
| `projectHits.maxScore` | number |  |
| `projectHits.totalCount` | number |  |
| `taskHits.hasHits` | boolean |  |
| `taskHits.hits[].entity.baseType` | string |  |
| `taskHits.hits[].entity.correlationId` | string |  |
| `taskHits.hits[].entity.createdBy` | string |  |
| `taskHits.hits[].entity.description` | string |  |
| `taskHits.hits[].entity.id` | string |  |
| `taskHits.hits[].entity.indexTime` | date |  |
| `taskHits.hits[].entity.isExternal` | boolean |  |
| `taskHits.hits[].entity.isHiddenForConnectUsers` | boolean |  |
| `taskHits.hits[].entity.isOpen` | boolean |  |
| `taskHits.hits[].entity.isPrio` | boolean |  |
| `taskHits.hits[].entity.lists[]` | string |  |
| `taskHits.hits[].entity.name` | string |  |
| `taskHits.hits[].entity.plannedDuration` | number |  |
| `taskHits.hits[].entity.project.createdBy` | string |  |
| `taskHits.hits[].entity.project.id` | string |  |
| `taskHits.hits[].entity.project.isBillableByDefault` | boolean |  |
| `taskHits.hits[].entity.project.isExternal` | boolean |  |
| `taskHits.hits[].entity.project.isPrivate` | boolean |  |
| `taskHits.hits[].entity.project.members[].id` | string |  |
| `taskHits.hits[].entity.project.members[].projectRoleId` | string |  |
| `taskHits.hits[].entity.project.members[].projectRoleName` | string |  |
| `taskHits.hits[].entity.project.members[].userId` | string |  |
| `taskHits.hits[].entity.project.name` | string |  |
| `taskHits.hits[].entity.project.projectStatus.id` | string |  |
| `taskHits.hits[].entity.project.projectStatus.name` | string |  |
| `taskHits.hits[].entity.project.projectStatus.type` | string |  |
| `taskHits.hits[].entity.projectId` | string |  |
| `taskHits.hits[].entity.taskIdentifier` | string |  |
| `taskHits.hits[].entity.taskStatus.icon` | string |  |
| `taskHits.hits[].entity.taskStatus.name` | string |  |
| `taskHits.hits[].entity.taskStatus.type` | string |  |
| `taskHits.hits[].entity.typeOfWork.name` | string |  |
| `taskHits.hits[].entity.userStats[].lastOpened` | number |  |
| `taskHits.hits[].entity.userStats[].openCount` | number |  |
| `taskHits.hits[].entity.userStats[].userId` | string |  |
| `taskHits.hits[].entity.workspaceId` | string |  |
| `taskHits.hits[].highlights.name[]` | string |  |
| `taskHits.hits[].score` | number |  |
| `taskHits.hits[].type` | string |  |
| `taskHits.maxScore` | number |  |
| `taskHits.totalCount` | number |  |
| `taskListHits.hasHits` | boolean |  |
| `taskListHits.maxScore` | number |  |
| `taskListHits.totalCount` | number |  |
| `timeEntriesHits.hasHits` | boolean |  |
| `timeEntriesHits.maxScore` | number |  |
| `timeEntriesHits.totalCount` | number |  |
| `timeReportsHits.hasHits` | boolean |  |
| `timeReportsHits.maxScore` | number |  |
| `timeReportsHits.totalCount` | number |  |
| `top[].entity.baseType` | string |  |
| `top[].entity.correlationId` | string |  |
| `top[].entity.createdBy` | string |  |
| `top[].entity.description` | string |  |
| `top[].entity.id` | string |  |
| `top[].entity.indexTime` | date |  |
| `top[].entity.isExternal` | boolean |  |
| `top[].entity.isHiddenForConnectUsers` | boolean |  |
| `top[].entity.isOpen` | boolean |  |
| `top[].entity.isPrio` | boolean |  |
| `top[].entity.lists[]` | string |  |
| `top[].entity.name` | string |  |
| `top[].entity.plannedDuration` | number |  |
| `top[].entity.project.createdBy` | string |  |
| `top[].entity.project.id` | string |  |
| `top[].entity.project.isBillableByDefault` | boolean |  |
| `top[].entity.project.isExternal` | boolean |  |
| `top[].entity.project.isPrivate` | boolean |  |
| `top[].entity.project.members[].id` | string |  |
| `top[].entity.project.members[].projectRoleId` | string |  |
| `top[].entity.project.members[].projectRoleName` | string |  |
| `top[].entity.project.members[].userId` | string |  |
| `top[].entity.project.name` | string |  |
| `top[].entity.project.projectStatus.id` | string |  |
| `top[].entity.project.projectStatus.name` | string |  |
| `top[].entity.project.projectStatus.type` | string |  |
| `top[].entity.projectId` | string |  |
| `top[].entity.taskIdentifier` | string |  |
| `top[].entity.taskStatus.icon` | string |  |
| `top[].entity.taskStatus.name` | string |  |
| `top[].entity.taskStatus.type` | string |  |
| `top[].entity.typeOfWork.name` | string |  |
| `top[].entity.userStats[].lastOpened` | number |  |
| `top[].entity.userStats[].openCount` | number |  |
| `top[].entity.userStats[].userId` | string |  |
| `top[].entity.workspaceId` | string |  |
| `top[].highlights.name[]` | string |  |
| `top[].score` | number |  |
| `top[].type` | string |  |
| `totalCount` | number |  |
| `userHits.hasHits` | boolean |  |
| `userHits.maxScore` | number |  |
| `userHits.totalCount` | number |  |

## Native endpoint

Through the native Awork API, this operation is `GET /search` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-workspace.md) for the provider-specific parameters and requirements.

