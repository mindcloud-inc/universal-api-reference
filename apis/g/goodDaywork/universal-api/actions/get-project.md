# GoodDay.work: Get Project

Retrieves a single project from GoodDay.work.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=4uTCIw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "4uTCIw"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | GoodDay project ID. Default: `4uTCIw`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "endDate": "string",
      "estimate": 1,
      "health": 1,
      "id": "string",
      "momentCreated": "string",
      "name": "Ava Chen",
      "ownerUserId": "string",
      "parentProjectId": "string",
      "priority": 1,
      "progress": 1,
      "startDate": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Project description. |
| `endDate` | string | Project end date. |
| `estimate` | number | Project estimate in minutes. |
| `health` | number | Project health indicator. |
| `id` | string | Project ID. |
| `momentCreated` | string | Creation timestamp. |
| `name` | string | Project name. |
| `ownerUserId` | string | Project owner user ID. |
| `parentProjectId` | string | Parent project or folder ID. |
| `priority` | number | Project priority. |
| `progress` | number | Project progress percentage. |
| `startDate` | string | Project start date. |
| `status` | string | Project status label. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /project/:projectId` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

