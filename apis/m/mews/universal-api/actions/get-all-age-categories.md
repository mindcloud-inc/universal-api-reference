# Mews: Get All Age Categories

Retrieves age categories from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-age-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-age-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-age-categories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "classification": "string",
      "createdUtc": "2026-05-07T12:00:00.000Z",
      "externalIdentifier": "string",
      "id": "string",
      "isActive": true,
      "maximalAge": 1,
      "minimalAge": 1,
      "names": {},
      "serviceId": "string",
      "shortNames": {},
      "updatedUtc": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classification` | string | Age-category classification. |
| `createdUtc` | date | Creation timestamp in UTC. |
| `externalIdentifier` | string | External identifier when present. |
| `id` | string | Unique identifier of the age category. |
| `isActive` | boolean | Whether the age category is active. |
| `maximalAge` | number | Maximum age included in the category. |
| `minimalAge` | number | Minimum age included in the category. |
| `names` | object | Localized age-category names. |
| `serviceId` | string | Service identifier. |
| `shortNames` | object | Localized short names. |
| `updatedUtc` | date | Last update timestamp in UTC. |

## Native endpoint

Through the native Mews API, this operation is `POST /ageCategories/getAll` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-age-categories.md) for the provider-specific parameters and requirements.

