# Makeplans: Get Resource

Retrieves a resource from Makeplans.

```
GET https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/get-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/get-resource?connectionId=$CONNECTION_ID&resourceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/get-resource?${params}`, {
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
| `resourceId` | number | yes | The Makeplans resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "capacity": 1,
      "id": 1,
      "opening_hours_mon": [
        "string"
      ],
      "opening_hours_tue": [
        "string"
      ],
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `capacity` | number |  |
| `id` | number |  |
| `opening_hours_mon` | array<string> |  |
| `opening_hours_tue` | array<string> |  |
| `title` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Makeplans API, this operation is `GET /resources/:resourceId` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource.md) for the provider-specific parameters and requirements.

