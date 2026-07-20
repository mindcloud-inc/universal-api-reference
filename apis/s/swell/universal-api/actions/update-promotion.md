# Swell: Update Promotion



```
PUT https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-promotion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-promotion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "discounts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-promotion', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "discounts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Swell promotion ID. |
| `discounts[]` | array<object> | yes | Promotion discount rules. |
| `name` | string | no | The promotion name. |
| `active` | boolean | no | Whether the promotion is active. |
| `dateStart` | date | no | The promotion start timestamp. |
| `dateEnd` | date | no | The promotion end timestamp. |
| `description` | string | no | The promotion description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateEnd": "2026-05-07T12:00:00.000Z",
      "dateStart": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "discounts": [
        {
          "type": "string",
          "valueFixed": 1,
          "valueType": "string"
        }
      ],
      "id": "string",
      "name": "Ava Chen",
      "useCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `dateEnd` | date |  |
| `dateStart` | date |  |
| `description` | string |  |
| `discounts[].type` | string |  |
| `discounts[].valueFixed` | number |  |
| `discounts[].valueType` | string |  |
| `id` | string |  |
| `name` | string |  |
| `useCount` | number |  |

## Native endpoint

Through the native Swell API, this operation is `PUT /promotions/:id` (base URL `https://api.swell.store`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-promotion.md) for the provider-specific parameters and requirements.

