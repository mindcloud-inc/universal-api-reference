# Anabix CRM: Get Deal

Retrieves a deal from Anabix CRM.

```
GET https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-deal?connectionId=$CONNECTION_ID&data.idDeal=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data.idDeal": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-deal?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.idDeal` | number | yes |  |

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

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

