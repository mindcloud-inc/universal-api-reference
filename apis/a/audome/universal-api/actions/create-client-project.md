# Audome: Create Client Project



```
POST https://connect.mindcloud.co/v1/universal/audome/latest/actions/create-client-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/audome/latest/actions/create-client-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerName": "Test",
  "title": "MindCloud Client Project Validation"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/audome/latest/actions/create-client-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerName": "Test",
    "title": "MindCloud Client Project Validation"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerName` | string | yes | Customer display name. Example: `Test`. |
| `note` | string | no | Optional project note. Example: `Validation run`. |
| `password` | string | no | Optional project password. Example: `project-password`. |
| `sentAt` | date | no | Optional sent timestamp. Example: `2026-04-03T12:00:00Z`. |
| `title` | string | yes | Project title. Example: `MindCloud Client Project Validation`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Audome API returns.

## Native endpoint

Through the native Audome API, this operation is `POST /client-projects` (base URL `https://app.audome.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client-project.md) for the provider-specific parameters and requirements.

