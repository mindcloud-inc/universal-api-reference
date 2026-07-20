# PPM Express: Get Project Key Date



```
GET https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-project-key-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PPM Express `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-project-key-date?connectionId=$CONNECTION_ID&projectId=df837bfe-1b68-497c-afe6-3e3ee50eb95e&keyDateId=e598bbf2-fa20-4a1f-82eb-50aea7f9ec2a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "df837bfe-1b68-497c-afe6-3e3ee50eb95e",
  "keyDateId": "e598bbf2-fa20-4a1f-82eb-50aea7f9ec2a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-project-key-date?${params}`, {
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
| `keyDateId` | string | yes | Default: `e598bbf2-fa20-4a1f-82eb-50aea7f9ec2a`. |

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
| `data` | object | The requested project key date. |

## Native endpoint

Through the native PPM Express API, this operation is `GET /@:tenantName/v1.0/projects/:projectId/keydates/:keyDateId` (base URL `https://api-us.ppm.express`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-key-date.md) for the provider-specific parameters and requirements.

