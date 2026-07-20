# Strava: Get Upload

Retrieves an activity upload from Strava.

```
GET https://connect.mindcloud.co/v1/universal/strava/latest/actions/get-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strava `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strava/latest/actions/get-upload?connectionId=$CONNECTION_ID&uploadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uploadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strava/latest/actions/get-upload?${params}`, {
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
| `uploadId` | string | yes | The identifier of the upload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Strava API returns.

## Native endpoint

Through the native Strava API, this operation is `GET /uploads/:uploadId` (base URL `https://www.strava.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload.md) for the provider-specific parameters and requirements.

