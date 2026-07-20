# Google Cloud Document AI: Get Location

Retrieves a location from Google Cloud Document AI.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/get-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/get-location?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/get-location?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Cloud Document AI API returns.

## Native endpoint

Through the native Google Cloud Document AI API, this operation is `GET /v1/projects/:projectsId/locations/:locationsId` (base URL `https://documentai.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location.md) for the provider-specific parameters and requirements.

