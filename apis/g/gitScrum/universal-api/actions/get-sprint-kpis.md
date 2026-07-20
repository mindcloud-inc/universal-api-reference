# GitScrum: Get Sprint KPIs

Retrieves KPI metrics for a GitScrum sprint.

```
GET https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-sprint-kpis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitScrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-sprint-kpis?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-sprint-kpis?${params}`, {
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
| `companySlug` | string | no |  |
| `projectSlug` | string | no |  |
| `slug` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "kpis": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `kpis` | object |  |

## Native endpoint

Through the native GitScrum API, this operation is `GET /sprints/:slug/kpis` (base URL `https://services.gitscrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sprint-kpis.md) for the provider-specific parameters and requirements.

