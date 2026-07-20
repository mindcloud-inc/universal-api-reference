# Mixpanel: List Saved Cohorts

Retrieves saved cohorts from Mixpanel.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-saved-cohorts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-saved-cohorts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-saved-cohorts?${params}`, {
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
| `projectId` | number | no | Required when using service-account authentication for the Query API. |
| `workspaceId` | number | no | Optional workspace ID when the cohort lives in a workspace context. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "created": "string",
      "description": "string",
      "id": 1,
      "isVisible": 1,
      "name": "Ava Chen",
      "projectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of users currently in the cohort. |
| `created` | string | Cohort creation timestamp. |
| `description` | string | Cohort description text. |
| `id` | number | Cohort ID. |
| `isVisible` | number | Visibility flag where 0 means hidden and 1 means visible. |
| `name` | string | Cohort name. |
| `projectId` | number | Mixpanel project ID that owns the cohort. |

## Native endpoint

Through the native Mixpanel API, this operation is `POST /query/cohorts/list` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-saved-cohorts.md) for the provider-specific parameters and requirements.

