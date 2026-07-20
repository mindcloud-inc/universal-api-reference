# Pinata: Add File To Group

Updates a Pinata group by adding a file.

```
PUT https://connect.mindcloud.co/v1/universal/pinata/latest/actions/add-file-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/add-file-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string",
  "id": "string",
  "network": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinata/latest/actions/add-file-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string",
    "id": "string",
    "network": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | ID of the file to add to the group. |
| `id` | string | yes | ID of the target group. |
| `network` | string | yes | Target network (`public` or `private`). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Provider returned null data for the saved successful update run. |

## Native endpoint

Through the native Pinata API, this operation is `PUT /v3/groups/:network/:id/ids/:fileId` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-file-to-group.md) for the provider-specific parameters and requirements.

