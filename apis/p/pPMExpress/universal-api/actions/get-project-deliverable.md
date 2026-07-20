# PPM Express: Get Project Deliverable



```
GET https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-project-deliverable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PPM Express `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-project-deliverable?connectionId=$CONNECTION_ID&projectId=df837bfe-1b68-497c-afe6-3e3ee50eb95e&deliverableId=9989ec64-b3d4-4899-ae73-3262dc653d05" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "df837bfe-1b68-497c-afe6-3e3ee50eb95e",
  "deliverableId": "9989ec64-b3d4-4899-ae73-3262dc653d05"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-project-deliverable?${params}`, {
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
| `projectId` | string | yes | Default: `df837bfe-1b68-497c-afe6-3e3ee50eb95e`. |
| `deliverableId` | string | yes | Default: `9989ec64-b3d4-4899-ae73-3262dc653d05`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The requested project deliverable. |

## Native endpoint

Through the native PPM Express API, this operation is `GET /@:tenantName/v1.0/projects/:projectId/deliverables/:deliverableId` (base URL `https://api-us.ppm.express`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-deliverable.md) for the provider-specific parameters and requirements.

