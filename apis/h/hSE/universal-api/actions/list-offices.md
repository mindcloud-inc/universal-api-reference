# 4HSE: List Offices

Retrieves offices from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-offices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-offices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-offices?${params}`, {
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
| `filter` | object | no | Office filters. |
| `filter.projectId` | string | no | Find offices within a company. |
| `filter.name` | string | no | Search an office by name within a project. |
| `filter.officeTypeIcon` | string | no | Filter by office type icon. |
| `history` | boolean | no | Include historized entries when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "country": "string",
      "createdAt": 1,
      "description": "string",
      "locality": "Ava Chen",
      "name": "Ava Chen",
      "officeId": "string",
      "officeTypeIcon": "string",
      "officeTypeId": "string",
      "ownedActive": true,
      "parentActive": 1,
      "permission": "string",
      "postalCode": "string",
      "projectId": "string",
      "projectName": "Ava Chen",
      "projectStatus": "string",
      "projectType": "string",
      "region": "string",
      "status": "string",
      "street": "string",
      "taxCode": "string",
      "updatedAt": 1,
      "vat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Alternative identifier code for the office. |
| `country` | string | ISO 3166-1 alpha-2 country code. |
| `createdAt` | number | Creation timestamp. |
| `description` | string | Optional free-text description. |
| `locality` | string | City or locality. |
| `name` | string | Name of the office or work location. |
| `officeId` | string | Unique identifier of the office. |
| `officeTypeIcon` | string | Visual type of the office. |
| `officeTypeId` | string | Custom office type identifier. |
| `ownedActive` | boolean | Whether this office is currently active in its validity period. |
| `parentActive` | number | Whether the parent project is currently active. |
| `permission` | string | Permission level for the current user. |
| `postalCode` | string | Postal code. |
| `projectId` | string | The project (company) this office belongs to. |
| `projectName` | string | Name of the project (company) this office belongs to. |
| `projectStatus` | string | Status of the parent project. |
| `projectType` | string | Type of the parent project. |
| `region` | string | Region or province code. |
| `status` | string | Office status. |
| `street` | string | Street address. |
| `taxCode` | string | Tax code of the work location. |
| `updatedAt` | number | Last modification timestamp. |
| `vat` | string | VAT number of the work location. |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/office/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-offices.md) for the provider-specific parameters and requirements.

