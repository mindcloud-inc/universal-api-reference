# Productlane: Upvote Project

Creates a project upvote in the Productlane portal.

```
POST https://connect.mindcloud.co/v1/universal/productlane/latest/actions/upvote-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/upvote-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "stage3-portal-test@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/upvote-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "stage3-portal-test@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | End-user email for the upvote. Example: `stage3-portal-test@example.com`. |
| `issueId` | string | no | Issue ID to upvote. Example: `issue-id`. |
| `projectId` | string | no | Project ID to upvote. Example: `project-id`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Productlane API returns.

## Native endpoint

Through the native Productlane API, this operation is `POST /portal/upvotes` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upvote-project.md) for the provider-specific parameters and requirements.

