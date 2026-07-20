# Mews: Get All Resource Features

Retrieves resource features from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-resource-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-resource-features?connectionId=$CONNECTION_ID&limit=25&offset=0&serviceIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "serviceIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-resource-features?${params}`, {
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
| `serviceIds[]` | array<string> | yes | Service identifiers whose resource features should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classification": "string",
      "createdUtc": "2026-05-07T12:00:00.000Z",
      "descriptions": {},
      "id": "string",
      "isActive": true,
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
| `classification` | string | Resource-feature classification. |
| `createdUtc` | date | Creation timestamp in UTC. |
| `descriptions` | object | Localized descriptions. |
| `id` | string | Unique identifier of the resource feature. |
| `isActive` | boolean | Whether the resource feature is active. |
| `names` | object | Localized feature names. |
| `serviceId` | string | Service identifier. |
| `shortNames` | object | Localized short names. |
| `updatedUtc` | date | Last update timestamp in UTC. |

## Native endpoint

Through the native Mews API, this operation is `POST /resourceFeatures/getAll` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-resource-features.md) for the provider-specific parameters and requirements.

