# Formstack Documents: Merge Data Route

Merges data through a data route in Formstack Documents.

```
POST https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/merge-data-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/merge-data-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/merge-data-route', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `download` | string | no | Return merged file contents when set to 1 |
| `id` | string | yes | ID of the data route to merge |
| `key` | string | yes | Merge key from the data route URL |
| `test` | string | no | Use test mode when set to 1 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {}
      ],
      "success": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `files` | array<object> | Returned when download is requested and the route produces multiple merged files. |
| `success` | number | Provider success flag returned when download is not requested. |

## Native endpoint

Through the native Formstack Documents API, this operation is `POST https://www.webmerge.me/route/:id/:key` (base URL `https://www.webmerge.me/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-data-route.md) for the provider-specific parameters and requirements.

