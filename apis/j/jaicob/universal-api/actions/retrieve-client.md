# Jaicob: Retrieve Client



```
GET https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-client?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-client?${params}`, {
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
| `id` | string | yes | Client identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "bannerImage": "string",
      "companyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "details": {},
      "id": "string",
      "locations": [
        {}
      ],
      "ownerLocations": [
        {}
      ],
      "slug": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `bannerImage` | string |  |
| `companyName` | string |  |
| `createdAt` | date |  |
| `details` | object |  |
| `id` | string |  |
| `locations` | array<object> |  |
| `ownerLocations` | array<object> |  |
| `slug` | string |  |
| `updatedAt` | date |  |
| `website` | string |  |

## Native endpoint

Through the native Jaicob API, this operation is `GET /clients/public/[:id]` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-client.md) for the provider-specific parameters and requirements.

