# Simplesat: List Surveys

Retrieves surveys from Simplesat.

```
GET https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-surveys?${params}`, {
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
| `pageSize` | number | no | The number of surveys to return per page |
| `page` | number | no | The page number to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand_name": "Ava Chen",
      "id": 1,
      "metric": "string",
      "name": "Ava Chen",
      "survey_token": "string",
      "survey_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand_name` | string |  |
| `id` | number |  |
| `metric` | string |  |
| `name` | string |  |
| `survey_token` | string |  |
| `survey_type` | string |  |

## Native endpoint

Through the native Simplesat API, this operation is `GET /api/v1/surveys` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

