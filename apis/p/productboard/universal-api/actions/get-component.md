# Productboard: Get Component

Retrieves a component from your Productboard workspace.

```
GET https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-component
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-component?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-component?${params}`, {
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
| `id` | string | yes | Component ID from Productboard. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "links": {},
      "name": "Ava Chen",
      "owner": {},
      "parent": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Rich-text component description. |
| `id` | string | Productboard component identifier. |
| `links` | object | API and HTML links for the component. |
| `name` | string | Component name. |
| `owner` | object | Owner information. |
| `parent` | object | Parent product reference. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Productboard API, this operation is `GET /components/:id` (base URL `https://api.productboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-component.md) for the provider-specific parameters and requirements.

