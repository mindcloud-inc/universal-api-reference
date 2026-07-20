# DoneDone: List Project Statuses

Retrieves project statuses from DoneDone.

```
GET https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/list-project-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DoneDone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/list-project-statuses?connectionId=$CONNECTION_ID&accountId=1&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/list-project-statuses?${params}`, {
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
| `accountId` | number | yes | DoneDone account ID. |
| `projectId` | number | yes | DoneDone internal project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Status color token. |
| `id` | number | Status ID. |
| `name` | string | Status name. |

## Native endpoint

Through the native DoneDone API, this operation is `GET /:account_id/internal-projects/:internal_project_id/statuses` (base URL `https://2.donedone.com/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-statuses.md) for the provider-specific parameters and requirements.

