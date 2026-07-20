# Veracity Learning: Delete State Document

Deletes a state document from Veracity Learning.

```
DELETE https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/delete-state-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/delete-state-document?connectionId=$CONNECTION_ID&activityId=string&agent=%5Bobject%20Object%5D&stateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "string",
  "agent": "[object Object]",
  "stateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/delete-state-document?${params}`, {
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
| `activityId` | string | yes | Target activity IRI. |
| `agent` | object | yes | xAPI Agent JSON object identifying the learner or actor. |
| `registration` | string | no | Optional registration UUID. |
| `stateId` | string | yes | Exact state document identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Veracity Learning API returns.

## Native endpoint

Through the native Veracity Learning API, this operation is `DELETE /activities/state` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-state-document.md) for the provider-specific parameters and requirements.

