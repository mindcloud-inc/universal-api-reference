# Kite Suite: Update Release



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-release" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "id": "string",
  "title": "string",
  "description": "string",
  "startDate": "string",
  "releaseDate": "string",
  "manager": "string",
  "status": "string",
  "resources[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-release', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "id": "string",
    "title": "string",
    "description": "string",
    "startDate": "string",
    "releaseDate": "string",
    "manager": "string",
    "status": "string",
    "resources[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | yes | Release ID |
| `title` | string | yes |  |
| `description` | string | yes |  |
| `startDate` | string | yes |  |
| `releaseDate` | string | yes |  |
| `manager` | string | yes |  |
| `status` | string | yes |  |
| `resources[]` | array | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdBy": "string",
      "description": "string",
      "isTrashed": true,
      "manager": "string",
      "projectID": "string",
      "releaseDate": "string",
      "resources": [
        "string"
      ],
      "startDate": "string",
      "status": "string",
      "tasks": [
        "string"
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the Release |
| `createdBy` | string | creator of the this Release |
| `description` | string |  |
| `isTrashed` | boolean | trash status of this Release |
| `manager` | string | manager of the this Release |
| `projectID` | string | project ID of Release |
| `releaseDate` | string |  |
| `resources` | array |  |
| `startDate` | string |  |
| `status` | string |  |
| `tasks` | array |  |
| `title` | string | title of Release |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/release/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-release.md) for the provider-specific parameters and requirements.

