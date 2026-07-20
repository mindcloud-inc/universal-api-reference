# Mews: Get All Resources

Retrieves resources from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-resources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-resources?${params}`, {
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
      "createdUtc": "2026-05-07T12:00:00.000Z",
      "data": {},
      "descriptions": {},
      "directions": {},
      "enterpriseId": "string",
      "externalNames": {},
      "id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "parentResourceId": "string",
      "state": "string",
      "updatedUtc": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdUtc` | date | Creation timestamp in UTC. |
| `data` | object | Resource type-specific payload. |
| `descriptions` | object | Localized descriptions. |
| `directions` | object | Localized directions payload. |
| `enterpriseId` | string | Enterprise identifier. |
| `externalNames` | object | External names payload. |
| `id` | string | Unique identifier of the resource. |
| `isActive` | boolean | Whether the resource is active. |
| `name` | string | Resource name. |
| `parentResourceId` | string | Parent resource identifier when present. |
| `state` | string | Resource state. |
| `updatedUtc` | date | Last update timestamp in UTC. |

## Native endpoint

Through the native Mews API, this operation is `POST /resources/getAll` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-resources.md) for the provider-specific parameters and requirements.

