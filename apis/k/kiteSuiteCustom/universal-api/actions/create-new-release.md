# Kite Suite: Create new release



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-release" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "title": "string",
  "description": "string",
  "startDate": "string",
  "releaseDate": "string",
  "projectID": "string",
  "manager": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-release', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "title": "string",
    "description": "string",
    "startDate": "string",
    "releaseDate": "string",
    "projectID": "string",
    "manager": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `title` | string | yes |  |
| `description` | string | yes |  |
| `startDate` | string | yes |  |
| `releaseDate` | string | yes |  |
| `projectID` | string | yes |  |
| `manager` | string | yes |  |

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

Through the native Kite Suite API, this operation is `POST /api/v1/release` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-release.md) for the provider-specific parameters and requirements.

