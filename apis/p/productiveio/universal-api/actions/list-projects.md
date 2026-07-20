# Productive.io: List Projects

Retrieves projects from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-projects?${params}`, {
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
      "attributes": {
        "archivedAt": "string",
        "createdAt": "string",
        "customFields": "string",
        "duplicationStatus": "string",
        "lastActivityAt": "string",
        "name": "Ava Chen",
        "number": "string",
        "pageCustomFieldsIds": "string",
        "pageCustomFieldsPositions": "string",
        "projectColorId": "string",
        "projectNumber": "string",
        "projectTypeId": 1,
        "sampleData": true,
        "taskCustomFieldsIds": "string",
        "taskCustomFieldsPositions": "string",
        "template": true
      },
      "id": "string",
      "relationships": {
        "company": {
          "meta": {
            "included": true
          }
        },
        "customFieldAttachments": {
          "meta": {
            "included": true
          }
        },
        "customFieldPeople": {
          "meta": {
            "included": true
          }
        },
        "lastActor": {
          "meta": {
            "included": true
          }
        },
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "projectManager": {
          "meta": {
            "included": true
          }
        },
        "templateObject": {
          "meta": {
            "included": true
          }
        },
        "workflow": {
          "meta": {
            "included": true
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.archivedAt` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.customFields` | string |  |
| `attributes.duplicationStatus` | string |  |
| `attributes.lastActivityAt` | string |  |
| `attributes.name` | string |  |
| `attributes.number` | string |  |
| `attributes.pageCustomFieldsIds` | string |  |
| `attributes.pageCustomFieldsPositions` | string |  |
| `attributes.projectColorId` | string |  |
| `attributes.projectNumber` | string |  |
| `attributes.projectTypeId` | number |  |
| `attributes.sampleData` | boolean |  |
| `attributes.taskCustomFieldsIds` | string |  |
| `attributes.taskCustomFieldsPositions` | string |  |
| `attributes.template` | boolean |  |
| `id` | string |  |
| `relationships.company.meta.included` | boolean |  |
| `relationships.customFieldAttachments.meta.included` | boolean |  |
| `relationships.customFieldPeople.meta.included` | boolean |  |
| `relationships.lastActor.meta.included` | boolean |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.projectManager.meta.included` | boolean |  |
| `relationships.templateObject.meta.included` | boolean |  |
| `relationships.workflow.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /projects` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

