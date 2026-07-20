# Anabix CRM: Manage Contact Lists

Updates contact list memberships in Anabix CRM.

```
PUT https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/manage-contact-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/manage-contact-lists" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.idContact": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/manage-contact-lists', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.idContact": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.idContact` | number | yes |  |
| `data.addTo[]` | array<number> | no |  |
| `data.removeFrom[]` | array<number> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "idContact": 1,
      "lists": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `idContact` | number | Anabix contact ID. |
| `lists` | array<number> | List IDs currently assigned to the contact. |

## Native endpoint

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/manage-contact-lists.md) for the provider-specific parameters and requirements.

