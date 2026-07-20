# DatoCMS: Get Record Current vs Published State



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-record-current-vs-published-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-record-current-vs-published-state?connectionId=$CONNECTION_ID&itemId=BrD64oBjT5y3MRXApeRNrA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "BrD64oBjT5y3MRXApeRNrA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-record-current-vs-published-state?${params}`, {
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
| `itemId` | string | yes | Example: `BrD64oBjT5y3MRXApeRNrA`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
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
| `relationships` | object |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /items/:itemId/current-vs-published-state` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record-current-vs-published-state.md) for the provider-specific parameters and requirements.

