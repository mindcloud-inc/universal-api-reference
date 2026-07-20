# HubSpot: Update Company by ID

Updates an existing company in HubSpot.

```
PUT https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-company-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-company-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-company-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string",
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | HubSpot company record ID to update. |
| `properties` | object | yes | Object of company properties to update, e.g. {"arr":"250000"}. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idProperty` | string | no | Unique property used to identify record instead of internal ID. |

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
| `url` | string | The HubSpot company URL. |

## Native endpoint

Through the native HubSpot API, this operation is `PATCH crm/v3/objects/companies/:companyId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company-by-id.md) for the provider-specific parameters and requirements.

