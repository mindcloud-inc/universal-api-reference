# Neon: Retrieve project consumption metrics

Retrieves project consumption metrics from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-consumption-history-per-project-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-consumption-history-per-project-v2?connectionId=$CONNECTION_ID&from=2026-05-07T12%3A00%3A00.000Z&to=2026-05-07T12%3A00%3A00.000Z&granularity=0&org_id=string&metrics%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-05-07T12:00:00.000Z",
  "to": "2026-05-07T12:00:00.000Z",
  "granularity": "0",
  "org_id": "string",
  "metrics[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-consumption-history-per-project-v2?${params}`, {
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
| `from` | date | yes | Neon API parameter from |
| `to` | date | yes | Neon API parameter to |
| `granularity` | list | yes | Neon API parameter granularity One of: `0`, `1`, `2`. |
| `org_id` | string | yes | Neon API parameter org_id |
| `metrics[]` | array<string> | yes | Neon API parameter metrics Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_ids[]` | array<string> | no | Neon API parameter project_ids Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "projects": [
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
| `pagination` | object |  |
| `projects` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `GET /consumption_history/v2/projects` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-consumption-history-per-project-v2.md) for the provider-specific parameters and requirements.

