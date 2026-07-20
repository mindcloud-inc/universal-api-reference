# Tolstoy: Get Project

Retrieves a specific project from Tolstoy.

```
GET https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tolstoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/get-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | Project id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "project": {
        "appKey": "string",
        "createdAt": "string",
        "id": "string",
        "name": "Ava Chen",
        "owner": "string",
        "publishId": "string",
        "stepsCount": 1,
        "stepsOrder": [
          "string"
        ],
        "tolstoyType": "string",
        "typeKey": "string",
        "updatedAt": "string",
        "verticalOrientation": true
      },
      "steps": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `project` | object |  |
| `project.appKey` | string |  |
| `project.createdAt` | string |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `project.owner` | string |  |
| `project.publishId` | string |  |
| `project.stepsCount` | number |  |
| `project.stepsOrder` | array<string> |  |
| `project.tolstoyType` | string |  |
| `project.typeKey` | string |  |
| `project.updatedAt` | string |  |
| `project.verticalOrientation` | boolean |  |
| `steps` | array<object> |  |

## Native endpoint

Through the native Tolstoy API, this operation is `GET /projects/:id` (base URL `https://api.gotolstoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

