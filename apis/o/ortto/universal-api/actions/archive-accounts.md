# Ortto: Archive Accounts



```
PUT https://connect.mindcloud.co/v1/universal/ortto/latest/actions/archive-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/archive-accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inclusion_ids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ortto/latest/actions/archive-accounts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inclusion_ids[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inclusion_ids[]` | array<string> | yes | Account IDs to archive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedOrganizations": 1,
      "scheduledOrganizations": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedOrganizations` | number |  |
| `scheduledOrganizations` | number |  |

## Native endpoint

Through the native Ortto API, this operation is `PUT /accounts/archive` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-accounts.md) for the provider-specific parameters and requirements.

