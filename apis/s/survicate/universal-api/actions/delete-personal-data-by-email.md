# Survicate: Delete Personal Data By Email

Deletes personal data by email from Survicate.

```
DELETE https://connect.mindcloud.co/v1/universal/survicate/latest/actions/delete-personal-data-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/survicate/latest/actions/delete-personal-data-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survicate/latest/actions/delete-personal-data-by-email?${params}`, {
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
| `email` | string | yes | The email address for which to delete all associated data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": {
        "deleted_insights_hub": 1,
        "deleted_respondents": 1,
        "total_deleted": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Confirmation message about the deletion result. |
| `result.deleted_insights_hub` | number | Number of deleted Insights Hub records. |
| `result.deleted_respondents` | number | Number of deleted Survicate respondent-related records. |
| `result.total_deleted` | number | Total number of deleted records across services. |

## Native endpoint

Through the native Survicate API, this operation is `DELETE /personal-data` (base URL `https://data-api.survicate.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-personal-data-by-email.md) for the provider-specific parameters and requirements.

