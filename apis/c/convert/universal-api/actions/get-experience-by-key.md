# Convert: Get Experience By Key

Retrieves an experience from Convert by key.

```
GET https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-experience-by-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-experience-by-key?connectionId=$CONNECTION_ID&projectId=string&experienceKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "experienceKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-experience-by-key?${params}`, {
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
| `projectId` | string | yes | Convert project ID. |
| `experienceKey` | string | yes | Convert experience key. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Convert API returns.

## Native endpoint

Through the native Convert API, this operation is `GET /accounts/:account_id/projects/:project_id/experiences/:experience_key` (base URL `https://api.convert.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experience-by-key.md) for the provider-specific parameters and requirements.

