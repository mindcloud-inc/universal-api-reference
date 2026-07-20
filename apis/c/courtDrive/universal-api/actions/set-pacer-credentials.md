# Court Drive: Set PACER Credentials



```
PUT https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/set-pacer-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/set-pacer-credentials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pacerUser": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/set-pacer-credentials', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pacerUser": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pacerUser` | string | yes | PACER username to store in CourtAPI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app_id": "string",
      "pacer_user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app_id` | string |  |
| `pacer_user` | string |  |

## Native endpoint

Through the native Court Drive API, this operation is `POST /pacer/credentials` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-pacer-credentials.md) for the provider-specific parameters and requirements.

