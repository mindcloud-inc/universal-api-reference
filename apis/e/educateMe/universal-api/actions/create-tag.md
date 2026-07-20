# EducateMe: Create Tag

Creates a new tag in EducateMe.

```
POST https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Onboarding Cohort",
  "category": "LOCATION"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Onboarding Cohort",
    "category": "LOCATION"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Tag title. Example: `Onboarding Cohort`. |
| `category` | string | yes | Tag category. Allowed values: LOCATION, OTHER, ROLE, DEPARTMENT, TEAM, FUNCTION, UNIT, PROBATION. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. Example: `LOCATION`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Tag category. |
| `id` | string | Tag ID. |
| `title` | string | Tag title. |

## Native endpoint

Through the native EducateMe API, this operation is `POST /tags` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

