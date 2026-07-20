# Microsoft Power BI: Get Import in Workspace



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-import-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-import-in-workspace?connectionId=$CONNECTION_ID&groupId=d5a55202-2ad7-487c-8c05-85a7092b4924&importId=d02b8896-e247-4d83-ae5a-014028cb0665" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "d5a55202-2ad7-487c-8c05-85a7092b4924",
  "importId": "d02b8896-e247-4d83-ae5a-014028cb0665"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-import-in-workspace?${params}`, {
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
| `groupId` | string | yes | Power BI workspace ID that contains the import. Example: `d5a55202-2ad7-487c-8c05-85a7092b4924`. |
| `importId` | string | yes | Power BI import ID to retrieve. Example: `d02b8896-e247-4d83-ae5a-014028cb0665`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "datasets": [
        {}
      ],
      "error": {},
      "id": "string",
      "importState": "string",
      "name": "Ava Chen",
      "reports": [
        {}
      ],
      "updatedDateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDateTime` | date | Import creation time. |
| `datasets` | array<object> | Datasets associated with this import. |
| `error` | object | Error details when the import fails. |
| `id` | string | Power BI import ID. |
| `importState` | string | Import state such as Publishing, Succeeded, or Failed. |
| `name` | string | Import name. |
| `reports` | array<object> | Reports associated with this import. |
| `updatedDateTime` | date | Import last update time. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]/imports/[:importId]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-import-in-workspace.md) for the provider-specific parameters and requirements.

