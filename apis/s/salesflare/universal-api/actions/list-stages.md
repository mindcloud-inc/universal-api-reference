# Salesflare: List Stages



```
GET https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesflare `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-stages?${params}`, {
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
| `orderBy` | string | no | Sort expression for stages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fullName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "order": 1,
      "pipeline": {},
      "probability": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fullName` | string |  |
| `id` | number |  |
| `name` | string |  |
| `order` | number |  |
| `pipeline` | object |  |
| `probability` | number |  |

## Native endpoint

Through the native Salesflare API, this operation is `GET stages` (base URL `https://api.salesflare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stages.md) for the provider-specific parameters and requirements.

