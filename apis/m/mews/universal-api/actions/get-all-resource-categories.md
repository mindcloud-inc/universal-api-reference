# Mews: Get All Resource Categories

Retrieves resource categories from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-resource-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-resource-categories?connectionId=$CONNECTION_ID&limit=25&offset=0&serviceIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "serviceIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-resource-categories?${params}`, {
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
| `serviceIds[]` | array<string> | yes | Service identifiers whose resource categories should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountingCategoryId": "string",
      "capacity": 1,
      "classification": "string",
      "descriptions": {},
      "enterpriseId": "string",
      "externalIdentifier": "string",
      "extraCapacity": 1,
      "id": "string",
      "isActive": true,
      "names": {},
      "ordering": 1,
      "serviceId": "string",
      "shortNames": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountingCategoryId` | string | Linked accounting-category identifier when present. |
| `capacity` | number | Base capacity. |
| `classification` | string | Category classification when present. |
| `descriptions` | object | Localized descriptions. |
| `enterpriseId` | string | Enterprise identifier. |
| `externalIdentifier` | string | External identifier when present. |
| `extraCapacity` | number | Extra capacity. |
| `id` | string | Unique identifier of the resource category. |
| `isActive` | boolean | Whether the resource category is active. |
| `names` | object | Localized category names. |
| `ordering` | number | Ordering value. |
| `serviceId` | string | Service identifier. |
| `shortNames` | object | Localized short names. |
| `type` | string | Resource-category type. |

## Native endpoint

Through the native Mews API, this operation is `POST /resourceCategories/getAll` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-resource-categories.md) for the provider-specific parameters and requirements.

