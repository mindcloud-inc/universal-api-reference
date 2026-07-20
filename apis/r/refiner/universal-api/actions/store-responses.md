# Refiner: Store Responses

Stores survey response data in Refiner.

```
POST https://connect.mindcloud.co/v1/universal/refiner/latest/actions/store-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refiner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/store-responses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refiner/latest/actions/store-responses', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Identify the user by your own user ID. |
| `email` | string | no | Identify the user by email address. |
| `formUuid` | string | yes | The Refiner form UUID that will own the stored response. |
| `date` | date | no | When the survey response was initially recorded. |
| `preventDuplicates` | boolean | no | Set to false to disable Refiner's duplicate prevention. |
| `responseData` | object | no | Key-value pairs where each key matches a Refiner question identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Refiner API, this operation is `POST /responses` (base URL `https://api.refiner.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/store-responses.md) for the provider-specific parameters and requirements.

