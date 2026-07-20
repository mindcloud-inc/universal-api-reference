# Reportei: Create Dashboard

Creates a new dashboard in Reportei.

```
POST https://connect.mindcloud.co/v1/universal/reportei/latest/actions/create-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/create-dashboard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "subtitle": "string",
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z",
  "templateId": 1,
  "integrationIds[]": [
    1
  ],
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reportei/latest/actions/create-dashboard', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "subtitle": "string",
    "start": "2026-05-07T12:00:00.000Z",
    "end": "2026-05-07T12:00:00.000Z",
    "templateId": 1,
    "integrationIds[]": [1],
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Título do dashboard. |
| `subtitle` | string | yes | Legenda do dashboard. |
| `start` | date | yes | Data de início da análise. |
| `end` | date | yes | Data de fim da análise. |
| `templateId` | number | yes | ID do template. |
| `integrationIds[]` | array<number> | yes | Array de IDs das integrações selecionadas. |
| `projectId` | number | yes | ID do projeto. |
| `comparisonStart` | date | no | Data de início da comparação. |
| `comparisonEnd` | date | no | Data de fim da comparação. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dashboard": {
        "external_url": "https://example.com",
        "id": 1,
        "internal_url": "https://example.com",
        "subtitle": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dashboard.external_url` | string | Public dashboard URL |
| `dashboard.id` | number | Dashboard identifier |
| `dashboard.internal_url` | string | Internal dashboard URL |
| `dashboard.subtitle` | string | Dashboard subtitle |
| `dashboard.title` | string | Dashboard title |

## Native endpoint

Through the native Reportei API, this operation is `POST /dashboards` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dashboard.md) for the provider-specific parameters and requirements.

