# XOi: Prepare Live Call



```
POST https://connect.mindcloud.co/v1/universal/xOi/latest/actions/prepare-live-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XOi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/prepare-live-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumber": "string",
  "namespace": "Ava Chen",
  "externalId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xOi/latest/actions/prepare-live-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumber": "string",
    "namespace": "Ava Chen",
    "externalId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNumber` | string | yes | XOi phone number input. |
| `namespace` | string | yes | XOi namespace input. |
| `externalId` | string | yes | XOi external id input. |
| `metadata` | string | no | XOi metadata json input. Default: `{}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callMetadataJSON": "string",
      "createdAt": "string",
      "createdBy": "string",
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
| `createdAt` | string |  |
| `createdBy` | string |  |
| `id` | string |  |
| `integrationEntityId` | object |  |
| `invitations` | array<object> |  |
| `visionLiveLink` | string |  |

## Native endpoint

Through the native XOi API, this operation is `POST https://gql-live-external.xoi.io/graphql` (base URL `https://gql-jobs-external.xoi.io/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/prepare-live-call.md) for the provider-specific parameters and requirements.

