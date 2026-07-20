# ClassDo: Get Viewer

Retrieves the current viewer from ClassDo.

```
GET https://connect.mindcloud.co/v1/universal/classDo/latest/actions/get-viewer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassDo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classDo/latest/actions/get-viewer?connectionId=$CONNECTION_ID&query=query%20GetViewerProfile%20%7B%20viewer%20%7B%20id%20name%20owner%20%7B%20id%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query GetViewerProfile { viewer { id name owner { id } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classDo/latest/actions/get-viewer?${params}`, {
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
| `query` | string | yes | GraphQL query payload. Default: `query GetViewerProfile { viewer { id name owner { id } } }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "viewer": {
          "id": "string",
          "name": "Ava Chen",
          "owner": {
            "id": "string"
          }
        }
      },
      "errors": [
        {
          "message": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.viewer.id` | string |  |
| `data.viewer.name` | string |  |
| `data.viewer.owner.id` | string |  |
| `errors[].message` | string |  |

## Native endpoint

Through the native ClassDo API, this operation is `POST /graphql` (base URL `https://api.classdo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-viewer.md) for the provider-specific parameters and requirements.

