# FormRobin: List Form Sessions

Retrieves form sessions for a specific form in FormRobin.

```
GET https://connect.mindcloud.co/v1/universal/formRobin/latest/actions/list-form-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FormRobin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formRobin/latest/actions/list-form-sessions?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formRobin/latest/actions/list-form-sessions?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browserName": "Ava Chen",
      "browserVersion": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deviceType": "string",
      "formFieldResponses": [
        {}
      ],
      "formId": 1,
      "id": 1,
      "ipAddress": "string",
      "landingPageUrl": "https://example.com",
      "operatingSystem": "string",
      "referrerUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "utmCampaign": "string",
      "utmContent": "string",
      "utmMedium": "string",
      "utmSource": "string",
      "utmTerm": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browserName` | string |  |
| `browserVersion` | string |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `deviceType` | string |  |
| `formFieldResponses` | array<object> |  |
| `formId` | number |  |
| `id` | number |  |
| `ipAddress` | string |  |
| `landingPageUrl` | string |  |
| `operatingSystem` | string |  |
| `referrerUrl` | string |  |
| `updatedAt` | date |  |
| `utmCampaign` | string |  |
| `utmContent` | string |  |
| `utmMedium` | string |  |
| `utmSource` | string |  |
| `utmTerm` | string |  |

## Native endpoint

Through the native FormRobin API, this operation is `GET /forms/{{id}}/sessions` (base URL `https://formrobin.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-sessions.md) for the provider-specific parameters and requirements.

