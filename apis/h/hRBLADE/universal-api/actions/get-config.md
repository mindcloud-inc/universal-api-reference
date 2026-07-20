# HRBLADE: Get Config



```
GET https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HRBLADE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-config?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-config?${params}`, {
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
      "code": 1,
      "error": true,
      "response": {
        "data": {
          "emailVars": [
            {
              "title": "ava@example.com",
              "value": "ava@example.com"
            }
          ],
          "generateQuestions": 1,
          "industries": [
            {
              "id": 1,
              "name": "Ava Chen"
            }
          ],
          "roles": [
            {
              "description": "string",
              "id": 1,
              "industryId": 1,
              "name": "Ava Chen"
            }
          ],
          "rolesCategories": [
            {
              "active": 1,
              "createdAt": "2026-05-07T12:00:00.000Z",
              "id": 1,
              "language": "string",
              "name": "Ava Chen",
              "updatedAt": "2026-05-07T12:00:00.000Z"
            }
          ],
          "subjects": [
            "string"
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `error` | boolean |  |
| `response.data.emailVars[].title` | string |  |
| `response.data.emailVars[].value` | string |  |
| `response.data.generateQuestions` | number |  |
| `response.data.industries[].id` | number |  |
| `response.data.industries[].name` | string |  |
| `response.data.roles[].description` | string |  |
| `response.data.roles[].id` | number |  |
| `response.data.roles[].industryId` | number |  |
| `response.data.roles[].name` | string |  |
| `response.data.rolesCategories[].active` | number |  |
| `response.data.rolesCategories[].createdAt` | date |  |
| `response.data.rolesCategories[].id` | number |  |
| `response.data.rolesCategories[].language` | string |  |
| `response.data.rolesCategories[].name` | string |  |
| `response.data.rolesCategories[].updatedAt` | date |  |
| `response.data.subjects[]` | string |  |

## Native endpoint

Through the native HRBLADE API, this operation is `GET /config` (base URL `https://api.hrblade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-config.md) for the provider-specific parameters and requirements.

