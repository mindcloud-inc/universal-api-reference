# Xata: Update project details



```
PUT https://connect.mindcloud.co/v1/universal/xata/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xata/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationID": "string",
  "projectID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xata/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationID": "string",
    "projectID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationID` | string | yes | Unique identifier of the organization containing the project |
| `projectID` | string | yes | Unique identifier of the project to update |
| `name` | string | no | New name for the project |
| `configuration` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configuration": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | object |  |
| `createdAt` | date | Timestamp when the project was created |
| `id` | string | Unique identifier for the project |
| `name` | string | Human-readable name of the project |
| `updatedAt` | date | Timestamp when the project was last updated |

## Native endpoint

Through the native Xata API, this operation is `PATCH /organizations/:organizationID/projects/:projectID` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

