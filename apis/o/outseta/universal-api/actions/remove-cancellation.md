# Outseta: Remove Cancellation

Removes an account cancellation in Outseta.

```
PUT https://connect.mindcloud.co/v1/universal/outseta/latest/actions/remove-cancellation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/remove-cancellation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountUid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/remove-cancellation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountUid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountUid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AccountStage": 1,
      "ClientIdentifier": "string",
      "Created": "string",
      "Name": "Ava Chen",
      "Uid": "string",
      "Updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountStage` | number |  |
| `ClientIdentifier` | string |  |
| `Created` | string |  |
| `Name` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `PUT /crm/accounts/removecancellation/:accountUid` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-cancellation.md) for the provider-specific parameters and requirements.

