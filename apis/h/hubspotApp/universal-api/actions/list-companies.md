# HubSpot: List Companies

Retrieves companies from HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-companies?${params}`, {
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
| `properties[]` | array<string> | no | Company properties to return in the response. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertiesWithHistory[]` | array<string> | no | Company properties to return with value history. |
| `associations[]` | array<string> | no | Company-associated object types to include as associated IDs. |
| `archived` | boolean | no | Whether to return only archived company records. |

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
| `archived` | boolean | Whether the company is archived. |
| `createdAt` | date | When the company was created. |
| `id` | string | The company record ID. |
| `properties` | object | The returned company properties. |
| `updatedAt` | date | When the company was last updated. |
| `url` | string | The HubSpot record URL. |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/objects/companies` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

