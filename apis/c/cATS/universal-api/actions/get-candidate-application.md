# CATS: Get Candidate Application

Retrieves a candidate application from CATS.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-candidate-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-candidate-application?connectionId=$CONNECTION_ID&applicationId=288125" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicationId": "288125"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-candidate-application?${params}`, {
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
| `applicationId` | number | yes | The ID of the candidate application to return. Example: `288125`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `GET /candidates/applications/:application_id` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-candidate-application.md) for the provider-specific parameters and requirements.

