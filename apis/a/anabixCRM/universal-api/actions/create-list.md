# Anabix CRM: Create List

Creates a new list in Anabix CRM.

```
POST https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.title` | string | yes | List title. Anabix requires this when creating a list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "customFields": [
        {}
      ],
      "idList": 1,
      "important": 1,
      "smartEmailing": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `customFields` | array<object> |  |
| `idList` | number | Anabix list ID. |
| `important` | number |  |
| `smartEmailing` | number |  |
| `title` | string | List title. |

## Native endpoint

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

