# Runn: Get Project



```
GET https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-project?${params}`, {
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
| `projectId` | number | yes | Runn project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": 1,
      "id": 1,
      "isArchived": true,
      "name": "Ava Chen",
      "rateCardId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | number | Associated client ID. |
| `id` | number | Project ID. |
| `isArchived` | boolean | Whether the project is archived. |
| `name` | string | Project name. |
| `rateCardId` | number | Associated rate card ID. |

## Native endpoint

Through the native Runn API, this operation is `GET /projects/{{projectId}}` (base URL `https://api.runn.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

