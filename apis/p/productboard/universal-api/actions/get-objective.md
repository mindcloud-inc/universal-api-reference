# Productboard: Get Objective

Retrieves an objective from your Productboard workspace.

```
GET https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-objective
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-objective?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-objective?${params}`, {
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
| `id` | string | yes | Objective ID from Productboard. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "level": "string",
      "links": {},
      "name": "Ava Chen",
      "owner": {},
      "parent": {},
      "state": "string",
      "status": {},
      "timeframe": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the objective is archived. |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Rich-text objective description. |
| `id` | string | Productboard objective identifier. |
| `level` | string | Objective level when present. |
| `links` | object | API and HTML links for the objective. |
| `name` | string | Objective name. |
| `owner` | object | Owner information. |
| `parent` | object | Parent objective reference when present. |
| `state` | string | Objective state when present. |
| `status` | object | Objective status object. |
| `timeframe` | object | Objective timeframe metadata. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Productboard API, this operation is `GET /objectives/:id` (base URL `https://api.productboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-objective.md) for the provider-specific parameters and requirements.

