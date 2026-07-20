# Frameshift: List Projects

Retrieves a list of projects from Frameshift.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-projects?${params}`, {
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
| `search` | string | no | The project name to fuzzy search for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "attributes": {
            "reference": "string",
            "referenceOrganism": "string"
          },
          "collaboratorCount": 1,
          "createdAt": "string",
          "description": "string",
          "id": 1,
          "isCollection": true,
          "isStarred": {},
          "isTemplate": true,
          "lastAccessed": {},
          "name": "Ava Chen",
          "nickname": {},
          "phiName": {},
          "primarySampleId": {},
          "privacyLevel": "string",
          "reference": "string",
          "roleTypeAccessLevel": 1,
          "roleTypeDisplayName": "Ava Chen",
          "sampleCount": 1,
          "taskCount": 1,
          "uid": "string",
          "updatedAt": "string",
          "variantCount": 1
        }
      ],
      "strictSearch": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].attributes.reference` | string |  |
| `data[].attributes.referenceOrganism` | string |  |
| `data[].collaboratorCount` | number |  |
| `data[].createdAt` | string |  |
| `data[].description` | string |  |
| `data[].id` | number |  |
| `data[].isCollection` | boolean |  |
| `data[].isStarred` | object |  |
| `data[].isTemplate` | boolean |  |
| `data[].lastAccessed` | object |  |
| `data[].name` | string |  |
| `data[].nickname` | object |  |
| `data[].phiName` | object |  |
| `data[].primarySampleId` | object |  |
| `data[].privacyLevel` | string |  |
| `data[].reference` | string |  |
| `data[].roleTypeAccessLevel` | number |  |
| `data[].roleTypeDisplayName` | string |  |
| `data[].sampleCount` | number |  |
| `data[].taskCount` | number |  |
| `data[].uid` | string |  |
| `data[].updatedAt` | string |  |
| `data[].variantCount` | number |  |
| `strictSearch` | boolean |  |

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

