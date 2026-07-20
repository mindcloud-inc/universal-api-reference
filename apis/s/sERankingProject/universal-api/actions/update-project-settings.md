# SE Ranking Project: Update Project Settings

Updates an existing project in SE Ranking.

```
PUT https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/update-project-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/update-project-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "site_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/update-project-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "site_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `site_id` | list<number> | yes | Project site identifier from SE Ranking. |
| `url` | string | no | Project website URL. |
| `title` | string | no | Project name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | array | The raw response body. The saved successful response was an empty array (HTTP 200). |

## Native endpoint

Through the native SE Ranking Project API, this operation is `PUT /sites/:site_id` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-settings.md) for the provider-specific parameters and requirements.

