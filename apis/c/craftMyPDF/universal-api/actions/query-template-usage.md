# CraftMyPDF: Query template usage

Retrieves template usage details from CraftMyPDF.

```
GET https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/query-template-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/query-template-usage?connectionId=$CONNECTION_ID&templateIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/query-template-usage?${params}`, {
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
| `templateIds` | string | yes |  |
| `startDate` | date | no |  |
| `endDate` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "2026-05-07T12:00:00.000Z",
      "results": [
        {}
      ],
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "templateIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | date |  |
| `results` | array<object> |  |
| `startDate` | date |  |
| `status` | string |  |
| `templateIds` | array<string> |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `GET /query-template-usage` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-template-usage.md) for the provider-specific parameters and requirements.

