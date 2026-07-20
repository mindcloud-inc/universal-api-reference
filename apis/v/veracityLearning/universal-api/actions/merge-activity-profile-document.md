# Veracity Learning: Merge Activity Profile Document

Updates an activity profile document in Veracity Learning by merging content.

```
PUT https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/merge-activity-profile-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/merge-activity-profile-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "string",
  "profileId": "string",
  "document": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/merge-activity-profile-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": "string",
    "profileId": "string",
    "document": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | string | yes | Target activity IRI. |
| `profileId` | string | yes | Exact activity profile document identifier. |
| `document` | object | yes | JSON document patch to merge into this activity profile. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Veracity Learning API returns.

## Native endpoint

Through the native Veracity Learning API, this operation is `POST /activities/profile` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-activity-profile-document.md) for the provider-specific parameters and requirements.

