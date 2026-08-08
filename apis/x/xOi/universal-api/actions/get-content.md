# XOi: Get Content



```
GET https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XOi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-content?connectionId=$CONNECTION_ID&contentIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contentIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-content?${params}`, {
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
| `contentIds[]` | array<string> | yes | XOi content ids input. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "jobIds": [
        {}
      ],
      "lengthBytes": 1,
      "mediaType": "string",
      "orgID": "string",
      "sha256hex": "string",
      "uploadedAt": "string",
      "uploader": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `jobIds` | array<object> |  |
| `lengthBytes` | number |  |
| `mediaType` | string |  |
| `orgID` | string |  |
| `sha256hex` | string |  |
| `uploadedAt` | string |  |
| `uploader` | string |  |

## Native endpoint

Through the native XOi API, this operation is `POST https://gql-content-external.xoi.io/graphql` (base URL `https://gql-jobs-external.xoi.io/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content.md) for the provider-specific parameters and requirements.

