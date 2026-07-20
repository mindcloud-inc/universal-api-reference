# UiPath Orchestrator: List machines



```
GET https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/list-machines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UiPath Orchestrator `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/list-machines?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/list-machines?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": 1,
      "LicenseKey": "string",
      "Name": "Ava Chen",
      "Type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | number |  |
| `LicenseKey` | string |  |
| `Name` | string |  |
| `Type` | string |  |

## Native endpoint

Through the native UiPath Orchestrator API, this operation is `GET /odata/Machines` (base URL `https://cloud.uipath.com/{{credentials.organizationName}}/{{credentials.tenantName}}/orchestrator_`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-machines.md) for the provider-specific parameters and requirements.

