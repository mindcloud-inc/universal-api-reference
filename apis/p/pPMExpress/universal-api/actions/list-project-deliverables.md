# PPM Express: List Project Deliverables



```
GET https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/list-project-deliverables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PPM Express `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/list-project-deliverables?connectionId=$CONNECTION_ID&projectId=df837bfe-1b68-497c-afe6-3e3ee50eb95e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "df837bfe-1b68-497c-afe6-3e3ee50eb95e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/list-project-deliverables?${params}`, {
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
| `projectId` | string | yes | The project ID whose deliverables to list. Default: `df837bfe-1b68-497c-afe6-3e3ee50eb95e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> | The deliverables in the selected project. |

## Native endpoint

Through the native PPM Express API, this operation is `GET /@:tenantName/v1.0/projects/:projectId/deliverables` (base URL `https://api-us.ppm.express`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-deliverables.md) for the provider-specific parameters and requirements.

