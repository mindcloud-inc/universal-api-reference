# Kite Suite: Get Release by Id



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-release-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-release-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-release-by-id?${params}`, {
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
| `id` | string | yes | Release ID |

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

Through the native Kite Suite API, this operation is `GET /api/v1/release/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-release-by-id.md) for the provider-specific parameters and requirements.

