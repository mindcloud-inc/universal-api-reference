# Microsoft Power BI: List Imports in Workspace



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-imports-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-imports-in-workspace?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-imports-in-workspace?${params}`, {
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
| `groupId` | string | yes | The workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectionType": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "datasets": [
        {
          "id": "string",
          "name": "Ava Chen",
          "webUrl": "https://example.com"
        }
      ],
      "error": {
        "code": "string"
      },
      "id": "string",
      "importState": "string",
      "name": "Ava Chen",
      "reports": [
        {
          "embedUrl": "https://example.com",
          "id": "string",
          "name": "Ava Chen",
          "webUrl": "https://example.com"
        }
      ],
      "source": "string",
      "updatedDateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionType` | string | The import connection type. |
| `createdDateTime` | date | Import creation date and time. |
| `datasets` | array<object> | The datasets associated with this import. |
| `datasets[].id` | string | The dataset ID associated with this import. |
| `datasets[].name` | string | The dataset name associated with this import. |
| `datasets[].webUrl` | string | The dataset web URL associated with this import. |
| `error` | object | Error details when the import has failed. |
| `error.code` | string | The import error code when the import has failed. |
| `id` | string | The import ID. |
| `importState` | string | The import upload state. |
| `name` | string | The import name. |
| `reports` | array<object> | The reports associated with this import. |
| `reports[].embedUrl` | string | The report embed URL associated with this import. |
| `reports[].id` | string | The report ID associated with this import. |
| `reports[].name` | string | The report name associated with this import. |
| `reports[].webUrl` | string | The report web URL associated with this import. |
| `source` | string | The import source. |
| `updatedDateTime` | date | Import last update date and time. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]/imports` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-imports-in-workspace.md) for the provider-specific parameters and requirements.

