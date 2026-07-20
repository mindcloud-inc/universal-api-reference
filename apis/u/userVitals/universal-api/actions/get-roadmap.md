# UserVitals: Get Roadmap

Retrieves a roadmap by ID from the roadmap API.

```
GET https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/get-roadmap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/get-roadmap?connectionId=$CONNECTION_ID&roadmapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roadmapId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/get-roadmap?${params}`, {
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
| `roadmapId` | string | yes | The roadmap unique id to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UserVitals API returns.

## Native endpoint

Through the native UserVitals API, this operation is `GET /roadmaps/:id` (base URL `https://app.roadmap.space/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-roadmap.md) for the provider-specific parameters and requirements.

