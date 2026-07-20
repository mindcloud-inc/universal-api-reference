# zipBoard: Create Review Link

Creates a new review link in zipBoard.

```
POST https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-review-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-review-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string",
  "projectId": "string",
  "secure": true,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-review-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string",
    "projectId": "string",
    "secure": true,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | File ID for the review link. |
| `projectId` | string | yes | Project ID for the review link. |
| `secure` | boolean | yes | Require the reviewer to sign up before review. |
| `type` | string | yes | Type of link: view&comment, fresh, or viewonly. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expireDate": "string",
      "fileid": "string",
      "id": "string",
      "projectid": "string",
      "secure": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expireDate` | string | Review link expiration date. |
| `fileid` | string | File identifier. |
| `id` | string | Review link identifier. |
| `projectid` | string | Project identifier. |
| `secure` | boolean | Whether the link is secure. |
| `type` | string | Review link type. |

## Native endpoint

Through the native zipBoard API, this operation is `POST /shareurl` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-review-link.md) for the provider-specific parameters and requirements.

