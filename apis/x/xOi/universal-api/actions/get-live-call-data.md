# XOi: Get Live Call Data



```
GET https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-live-call-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XOi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-live-call-data?connectionId=$CONNECTION_ID&liveCallId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "liveCallId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-live-call-data?${params}`, {
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
| `liveCallId` | string | yes | XOi live call id input. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callMetadataJSON": "string",
      "id": "string",
      "integrationEntityId": {},
      "invitations": [
        {}
      ],
      "visionLiveLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callMetadataJSON` | string |  |
| `id` | string |  |
| `integrationEntityId` | object |  |
| `invitations` | array<object> |  |
| `visionLiveLink` | string |  |

## Native endpoint

Through the native XOi API, this operation is `POST https://gql-live-external.xoi.io/graphql` (base URL `https://gql-jobs-external.xoi.io/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-live-call-data.md) for the provider-specific parameters and requirements.

