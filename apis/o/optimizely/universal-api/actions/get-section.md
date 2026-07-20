# Optimizely: Get Section

Retrieves a section from an Optimizely experiment.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-section?connectionId=$CONNECTION_ID&experimentId=1&sectionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experimentId": "1",
  "sectionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-section?${params}`, {
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
| `experimentId` | string | yes | The multivariate experiment id. Default: `1`. |
| `sectionId` | string | yes | The section id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "description": "string",
      "experimentId": 1,
      "id": 1,
      "name": "Ava Chen",
      "projectId": 1,
      "variations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `description` | string |  |
| `experimentId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `projectId` | number |  |
| `variations` | array<object> |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /experiments/{experimentId}/sections/{sectionId}` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-section.md) for the provider-specific parameters and requirements.

