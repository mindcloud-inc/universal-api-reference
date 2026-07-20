# Zoho Books: List Estimates



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-estimates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-estimates?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-estimates?${params}`, {
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
| `organizationId` | list | yes |  |
| `estimateNumber` | string | no | Example: `EST-00002`. |
| `referenceNumber` | string | no | Example: `QRT-12346`. |
| `customerName` | string | no | Example: `Mr. Gabriel Rodrigues`. |
| `total` | number | no | Example: `40.6`. |
| `customerId` | list | no |  |
| `itemId` | list | no |  |
| `itemName` | string | no | Example: `Codex Stage3 Item 20260311 Updated`. |
| `itemDescription` | string | no | Example: `Updated during Zoho Books Stage 3 validation`. |
| `expiryDate` | string | no | Example: `2026-03-31`. |
| `date` | date | no | Example: `2026-03-11`. |
| `status` | list | no | One of: `0`, `1`, `2`, `3`, `4`, `5`. |
| `filterBy` | list | no | One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `searchText` | string | no | Example: `EST-00002`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customField` | string | no | Example: `ApprovalStatus`. |
| `zcrmPotentialId` | number | no | Example: `460000000026049`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedDate": "string",
      "clientViewedTime": "string",
      "createdTime": "string",
      "currencyCode": "string",
      "currencyId": "string",
      "customerId": "string",
      "customerName": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "declinedDate": "string",
      "estimateId": "string",
      "estimateNumber": "string",
      "expiryDate": "string",
      "hasAttachment": true,
      "isViewedByClient": true,
      "lastModifiedTime": "string",
      "referenceNumber": "string",
      "salespersonId": "string",
      "salespersonName": "Ava Chen",
      "status": "string",
      "tags": [
        {}
      ],
      "templateId": "string",
      "templateType": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedDate` | string | Accepted date when present. |
| `clientViewedTime` | string | Client viewed timestamp when present. |
| `createdTime` | string | Creation timestamp. |
| `currencyCode` | string | Currency code. |
| `currencyId` | string | Currency identifier. |
| `customerId` | string | Customer identifier. |
| `customerName` | string | Customer name. |
| `date` | date | Estimate date. |
| `declinedDate` | string | Declined date when present. |
| `estimateId` | string | Unique identifier of the estimate. |
| `estimateNumber` | string | Estimate number. |
| `expiryDate` | string | Expiry date when present. |
| `hasAttachment` | boolean | Whether the estimate has an attachment. |
| `isViewedByClient` | boolean | Whether the estimate was viewed by the client. |
| `lastModifiedTime` | string | Last modification timestamp. |
| `referenceNumber` | string | External reference number. |
| `salespersonId` | string | Salesperson identifier when present. |
| `salespersonName` | string | Salesperson name when present. |
| `status` | string | Estimate status. |
| `tags` | array<object> | Tags associated with the estimate. |
| `templateId` | string | Template identifier. |
| `templateType` | string | Template type. |
| `total` | number | Estimate total amount. |

## Native endpoint

Through the native Zoho Books API, this operation is `GET /estimates` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-estimates.md) for the provider-specific parameters and requirements.

