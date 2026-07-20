# Fivetran: Create Connect Card

Creates a Connect Card for a connection in Fivetran.

```
POST https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/create-connect-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/create-connect-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/create-connect-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connectionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `connectCardConfig` | object | no | Connect Card configuration object. |
| `connectionId` | string | yes | The unique identifier for the connection within Fivetran. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectCardToken": "string",
      "connectCardUri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectCardToken` | string |  |
| `connectCardUri` | string |  |

## Native endpoint

Through the native Fivetran API, this operation is `POST /connections/[:connectionId]/connect-card` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-connect-card.md) for the provider-specific parameters and requirements.

