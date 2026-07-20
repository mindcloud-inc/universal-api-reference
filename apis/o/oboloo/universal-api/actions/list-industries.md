# Oboloo: List Industries

Retrieves industries from Oboloo.

```
GET https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-industries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oboloo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-industries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-industries?${params}`, {
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
| `search` | string | no | Filter industries by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "creator": {
        "documentId": {},
        "id": 1,
        "name": "Ava Chen",
        "userImage": {}
      },
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "status": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | object |  |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `creator.documentId` | object |  |
| `creator.id` | number |  |
| `creator.name` | string |  |
| `creator.userImage` | object |  |
| `deletedAt` | date |  |
| `id` | number |  |
| `status` | number |  |
| `updatedAt` | date |  |
| `value` | string |  |

## Native endpoint

Through the native Oboloo API, this operation is `GET /configuration/getIndustries` (base URL `https://mindcloudwizard20260330.oboloo.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-industries.md) for the provider-specific parameters and requirements.

