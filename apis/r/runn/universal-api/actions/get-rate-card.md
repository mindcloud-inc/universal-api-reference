# Runn: Get Rate Card



```
GET https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-rate-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-rate-card?connectionId=$CONNECTION_ID&rateCardId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rateCardId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-rate-card?${params}`, {
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
| `rateCardId` | number | yes | Runn rate card ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isArchived": true,
      "name": "Ava Chen",
      "rateType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Rate card ID. |
| `isArchived` | boolean | Whether the rate card is archived. |
| `name` | string | Rate card name. |
| `rateType` | string | Rate type. |

## Native endpoint

Through the native Runn API, this operation is `GET /rate-cards/{{rateCardId}}` (base URL `https://api.runn.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rate-card.md) for the provider-specific parameters and requirements.

