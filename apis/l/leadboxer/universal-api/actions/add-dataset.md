# Leadboxer: Add Dataset

Creates a new dataset in Leadboxer.

```
POST https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/add-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadboxer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/add-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "humanName": "Ava Chen",
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/add-dataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "humanName": "Ava Chen",
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The user email address. |
| `humanName` | string | yes | The display name for the dataset. |
| `timezone` | string | yes | The dataset timezone. |
| `userIds[]` | array<number> | no | Optional list of user IDs to associate. |
| `emails[]` | array<string> | no | Optional list of email addresses to associate. |
| `sendEmail` | boolean | no | Whether to send invitation emails. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadboxer API returns.

## Native endpoint

Through the native Leadboxer API, this operation is `POST /v1/datasets` (base URL `https://data.leadboxer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-dataset.md) for the provider-specific parameters and requirements.

