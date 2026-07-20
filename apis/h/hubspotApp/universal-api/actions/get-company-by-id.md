# HubSpot: Get Company by ID

Retrieves a company from HubSpot by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-company-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-company-by-id?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-company-by-id?${params}`, {
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
| `companyId` | string | yes | The company record ID. |
| `properties[]` | array<string> | no | Company properties to return in the response. Accepts multiple values in one string, delimited by `,`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertiesWithHistory[]` | array<string> | no | Company properties to return with value history. Accepts multiple values in one string, delimited by `,`. |
| `associations[]` | array<string> | no | Associated object types to include as associated IDs. Accepts multiple values in one string, delimited by `,`. |
| `archived` | boolean | no | Whether to return archived companies. |

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

Through the native HubSpot API, this operation is `GET crm/v3/objects/companies/:companyId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-by-id.md) for the provider-specific parameters and requirements.

