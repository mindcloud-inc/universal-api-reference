# SynergyCRM: Get Deal



```
GET https://connect.mindcloud.co/v1/universal/synergyCRM/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SynergyCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synergyCRM/latest/actions/get-deal?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synergyCRM/latest/actions/get-deal?${params}`, {
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
| `id` | string | yes | Record ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "links": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `links` | object |  |
| `relationships` | object |  |
| `type` | string |  |

## Native endpoint

Through the native SynergyCRM API, this operation is `GET /deals/:id` (base URL `https://app.synergycrm.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

