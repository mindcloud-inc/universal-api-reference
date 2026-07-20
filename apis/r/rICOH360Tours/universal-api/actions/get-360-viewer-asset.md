# RICOH360 Tours: Get 360 Viewer Asset



```
GET https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/get-360-viewer-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RICOH360 Tours `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/get-360-viewer-asset?connectionId=$CONNECTION_ID&contentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/get-360-viewer-asset?${params}`, {
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
| `contentId` | string | yes | Published content ID to generate a 360 viewer token for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "getPFViewerToken": {
          "token": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.getPFViewerToken.token` | string | Viewer token returned by the RICOH360 GraphQL API. |

## Native endpoint

Through the native RICOH360 Tours API, this operation is `POST /graphql` (base URL `https://bbomwcm27nhalfwjvwzy6qbrim.appsync-api.us-west-2.amazonaws.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-360-viewer-asset.md) for the provider-specific parameters and requirements.

