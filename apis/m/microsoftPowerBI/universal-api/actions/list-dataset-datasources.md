# Microsoft Power BI: List Dataset Datasources



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dataset-datasources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dataset-datasources?connectionId=$CONNECTION_ID&groupId=string&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string",
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dataset-datasources?${params}`, {
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
| `datasetId` | string | yes | The dataset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectionDetails": {},
      "datasourceId": "string",
      "datasourceType": "string",
      "gatewayId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionDetails` | object | Connection details for the datasource. |
| `datasourceId` | string | The datasource ID. |
| `datasourceType` | string | The datasource type. |
| `gatewayId` | string | The gateway ID. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]/datasets/[:datasetId]/datasources` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dataset-datasources.md) for the provider-specific parameters and requirements.

