# HubSpot: Get Deal by ID

Retrieves a deal from HubSpot by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-deal-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-deal-by-id?connectionId=$CONNECTION_ID&dealId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dealId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-deal-by-id?${params}`, {
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
| `dealId` | string | yes | The unique ID of the deal to retrieve. |
| `properties[]` | array<string> | no | Deal properties to return in the response. Accepts multiple values as an array. |
| `propertiesWithHistory[]` | array<string> | no | Deal properties to return with value history. |
| `associations` | string<string> | no | Associated object types to include as associated IDs. Accepts multiple values as an array. |
| `archived` | boolean | no | Whether to return archived deal records. |
| `idProperty` | string | no | The unique property to use for dealId instead of the default record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `id` | string |  |
| `properties` | object |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/objects/deals/:dealId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal-by-id.md) for the provider-specific parameters and requirements.

