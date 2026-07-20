# Perfit: Unsubscribe Contact



```
PUT https://connect.mindcloud.co/v1/universal/perfit/latest/actions/unsubscribe-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perfit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/perfit/latest/actions/unsubscribe-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": "string",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perfit/latest/actions/unsubscribe-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": "string",
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account` | string | yes | Perfit account name. |
| `contactId` | string | yes | Contact email or numeric ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "gender": "string",
      "id": 1,
      "inactivated": "2026-05-07T12:00:00.000Z",
      "interests": [
        {}
      ],
      "language": "string",
      "lastAction": "2026-05-07T12:00:00.000Z",
      "lastMailed": "2026-05-07T12:00:00.000Z",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "lists": [
        {}
      ],
      "preferredFormat": "string",
      "quality": 1,
      "source": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `customFields` | array<object> |  |
| `email` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `id` | number |  |
| `inactivated` | date |  |
| `interests` | array<object> |  |
| `language` | string |  |
| `lastAction` | date |  |
| `lastMailed` | date |  |
| `lastModified` | date |  |
| `lastName` | string |  |
| `lists` | array<object> |  |
| `preferredFormat` | string |  |
| `quality` | number |  |
| `source` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Perfit API, this operation is `POST /:account/contacts/:contactId/unsubscribe` (base URL `https://api.myperfit.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-contact.md) for the provider-specific parameters and requirements.

