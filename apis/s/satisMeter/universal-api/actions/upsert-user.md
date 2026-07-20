# SatisMeter: Upsert User



```
PUT https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/upsert-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SatisMeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/upsert-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "61fce0adea447e24ec27d606",
  "userId": "1234"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/upsert-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "61fce0adea447e24ec27d606",
    "userId": "1234"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Project ID. Example: `61fce0adea447e24ec27d606`. |
| `userId` | string | yes | User ID used on your end to uniquely identify the user. Example: `1234`. |
| `traits.name` | string | no | Optional user name stored in SatisMeter traits. |
| `traits.email` | string | no | Optional user email stored in SatisMeter traits. |
| `traits.createdAt` | date | no | Optional user creation timestamp stored in SatisMeter traits. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyDate` | date | no | Optional timestamp used to make the user eligible for an immediate survey display. Example: `2026-03-17T21:00:00Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SatisMeter API returns.

## Native endpoint

Through the native SatisMeter API, this operation is `POST /api/users` (base URL `https://app.satismeter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-user.md) for the provider-specific parameters and requirements.

