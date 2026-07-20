# Cinode: List Projects

Retrieves won projects for a company in Cinode.

```
GET https://connect.mindcloud.co/v1/universal/cinode/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cinode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/list-projects?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cinode/latest/actions/list-projects?${params}`, {
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
| `companyId` | number | yes | Cinode company ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "customerIdentifier": "string",
      "description": "string",
      "externalId": "string",
      "id": 1,
      "identifier": "string",
      "internalId": "string",
      "lastTouchDateTime": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "updatedDateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `createdDateTime` | date |  |
| `customerId` | number |  |
| `customerIdentifier` | string |  |
| `description` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `identifier` | string |  |
| `internalId` | string |  |
| `lastTouchDateTime` | date |  |
| `title` | string |  |
| `updatedDateTime` | date |  |

## Native endpoint

Through the native Cinode API, this operation is `GET /v0.1/companies/:companyId/projects` (base URL `https://api.cinode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

