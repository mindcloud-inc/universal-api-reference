# Diffy: Create Diff

Creates a screenshot diff in Diffy.

```
POST https://connect.mindcloud.co/v1/universal/diffy/latest/actions/create-diff
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/diffy/latest/actions/create-diff" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "snapshot1": 1,
  "snapshot2": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/diffy/latest/actions/create-diff', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "snapshot1": 1,
    "snapshot2": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Project ID. |
| `name` | string | no | Custom diff name. |
| `snapshot1` | number | yes | First screenshot ID. |
| `snapshot2` | number | yes | Second screenshot ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Created diff identifier. |

## Native endpoint

Through the native Diffy API, this operation is `POST /projects/:id/diffs` (base URL `https://app.diffy.website/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-diff.md) for the provider-specific parameters and requirements.

