# Veracity Learning: List State IDs

Lists state document IDs from Veracity Learning.

```
GET https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-state-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-state-ids?connectionId=$CONNECTION_ID&activityId=string&agent=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "string",
  "agent": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-state-ids?${params}`, {
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
| `activityId` | string | yes | Activity id associated with these state documents |
| `agent` | object | yes | Agent object associated with these state documents |
| `registration` | string | no | Registration id associated with these state documents |
| `since` | date | no | Only return state ids updated since this timestamp |

## Response

```json
{
  "success": true,
  "data": [
    {
      "stateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stateId` | string | State document identifier available for the requested activity and agent. |

## Native endpoint

Through the native Veracity Learning API, this operation is `GET /activities/state` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-state-ids.md) for the provider-specific parameters and requirements.

