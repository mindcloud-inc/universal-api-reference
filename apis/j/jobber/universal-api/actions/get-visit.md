# Jobber: Get Visit



```
GET https://connect.mindcloud.co/v1/universal/jobber/latest/actions/get-visit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobber/latest/actions/get-visit?connectionId=$CONNECTION_ID&visitId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "visitId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jobber/latest/actions/get-visit?${params}`, {
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
| `visitId` | string | yes | The Jobber visit ID used to find its job. |
| `columns` | string | no | Select the Jobber visit fields to return. Default: `["id","job.id"]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jobber API returns.

## Native endpoint

Through the native Jobber API, this operation is `POST graphql` (base URL `https://api.getjobber.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-visit.md) for the provider-specific parameters and requirements.

