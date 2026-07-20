# Anabix CRM: Create Deal

Creates a new deal in Anabix CRM.

```
POST https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.title": "string",
  "data.idContact": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.title": "string",
    "data.idContact": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.title` | string | yes |  |
| `data.idContact` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "body": "string",
      "city": "string",
      "code": "string",
      "completedDate": "2026-05-07T12:00:00.000Z",
      "contactIds": [
        1
      ],
      "country": "string",
      "customFields": [
        {}
      ],
      "deadline": "2026-05-07T12:00:00.000Z",
      "idDeal": 1,
      "idOwner": 1,
      "rating": "string",
      "revisionInfo": {},
      "status": "string",
      "street": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `body` | string |  |
| `city` | string |  |
| `code` | string |  |
| `completedDate` | date |  |
| `contactIds` | array<number> |  |
| `country` | string |  |
| `customFields` | array<object> |  |
| `deadline` | date |  |
| `idDeal` | number | Anabix deal ID. |
| `idOwner` | number |  |
| `rating` | string |  |
| `revisionInfo` | object |  |
| `status` | string |  |
| `street` | string |  |
| `title` | string | Deal title. |

## Native endpoint

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

