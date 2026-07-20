# MoneyBird: List Subscriptions

Retrieves subscriptions from MoneyBird.

```
GET https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoneyBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&administrationId=string&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "administrationId": "string",
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-subscriptions?${params}`, {
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
| `administrationId` | string | yes | Moneybird administration ID. |
| `contactId` | string | yes | Moneybird contact ID used to list subscriptions for one contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrationId": "string",
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "frequency": "string",
      "id": "string",
      "interval": 1,
      "productId": "string",
      "reference": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrationId` | string |  |
| `contactId` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `endDate` | date |  |
| `frequency` | string |  |
| `id` | string |  |
| `interval` | number |  |
| `productId` | string |  |
| `reference` | string |  |
| `startDate` | date |  |
| `state` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native MoneyBird API, this operation is `GET /:administrationId/subscriptions.json` (base URL `https://moneybird.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

