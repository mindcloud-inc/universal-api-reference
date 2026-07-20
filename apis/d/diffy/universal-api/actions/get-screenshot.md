# Diffy: Get Screenshot

Retrieves a single screenshot from Diffy.

```
GET https://connect.mindcloud.co/v1/universal/diffy/latest/actions/get-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffy/latest/actions/get-screenshot?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffy/latest/actions/get-screenshot?${params}`, {
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
| `id` | number | yes | Screenshot ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseline": true,
      "baseUrl": "https://example.com",
      "date": 1,
      "environment": "string",
      "name": "Ava Chen",
      "project": {},
      "state": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseline` | boolean | Whether this screenshot is the baseline. |
| `baseUrl` | string | Base URL for the screenshot run. |
| `date` | number | Screenshot creation timestamp. |
| `environment` | string | Screenshot environment. |
| `name` | string | Screenshot name. |
| `project` | object | Owning project summary. |
| `state` | number | Screenshot state code. |

## Native endpoint

Through the native Diffy API, this operation is `GET /snapshots/:id` (base URL `https://app.diffy.website/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-screenshot.md) for the provider-specific parameters and requirements.

