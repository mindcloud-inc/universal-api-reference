# SigningHub: Share Document Package

Shares a document package in SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/share-document-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/share-document-package" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": "11191524"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/share-document-package', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": "11191524"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | The document package to be shared. Example: `11191524`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        1
      ],
      "package_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<number> |  |
| `package_id` | number |  |

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages/:packageId/workflow` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/share-document-package.md) for the provider-specific parameters and requirements.

