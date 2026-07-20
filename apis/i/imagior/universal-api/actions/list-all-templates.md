# Imagior: List All Templates

Retrieves templates from Imagior.

```
GET https://connect.mindcloud.co/v1/universal/imagior/latest/actions/list-all-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Imagior `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imagior/latest/actions/list-all-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imagior/latest/actions/list-all-templates?${params}`, {
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
| `sort` | string | no | Sort by `createdAt` or `updatedAt`. Defaults to `updatedAt`. Default: `updatedAt`. |
| `order` | string | no | Sort order, either `asc` or `desc`. Defaults to `desc`. Default: `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the template was created. |
| `id` | string | Template ID. |
| `name` | string | Template name. |
| `updatedAt` | date | When the template was last updated. |

## Native endpoint

Through the native Imagior API, this operation is `GET /templates/all` (base URL `https://api.imagior.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-templates.md) for the provider-specific parameters and requirements.

