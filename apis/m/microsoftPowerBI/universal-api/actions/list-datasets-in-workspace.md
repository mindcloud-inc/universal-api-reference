# Microsoft Power BI: List Datasets in Workspace



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-datasets-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-datasets-in-workspace?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-datasets-in-workspace?${params}`, {
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
      "addRowsAPIEnabled": true,
      "configuredBy": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "createReportEmbedURL": "https://example.com",
      "description": "string",
      "id": "string",
      "isEffectiveIdentityRequired": true,
      "isEffectiveIdentityRolesRequired": true,
      "isOnPremGatewayRequired": true,
      "isRefreshable": true,
      "name": "Ava Chen",
      "qnaEmbedURL": "https://example.com",
      "targetStorageMode": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addRowsAPIEnabled` | boolean | Whether adding rows through the API is enabled. |
| `configuredBy` | string | The dataset owner. |
| `createdDate` | date | The dataset creation date and time. |
| `createReportEmbedURL` | string | The create report embed URL. |
| `description` | string | The dataset description. |
| `id` | string | The dataset ID. |
| `isEffectiveIdentityRequired` | boolean | Whether an effective identity is required. |
| `isEffectiveIdentityRolesRequired` | boolean | Whether identity roles are required. |
| `isOnPremGatewayRequired` | boolean | Whether an on-premises gateway is required. |
| `isRefreshable` | boolean | Whether the dataset is refreshable. |
| `name` | string | The dataset name. |
| `qnaEmbedURL` | string | The dataset Q&A embed URL. |
| `targetStorageMode` | string | The target storage mode. |
| `webUrl` | string | The dataset web URL. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]/datasets` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datasets-in-workspace.md) for the provider-specific parameters and requirements.

