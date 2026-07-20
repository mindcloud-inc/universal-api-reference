# Rithum DSCO: Get Catalog Change Log

Retrieves the catalog change log from Rithum DSCO.

```
GET https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-catalog-change-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum DSCO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-catalog-change-log?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-catalog-change-log?${params}`, {
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
| `startDate` | date | no | Start date for DSCO change-log filtering. |
| `endDate` | date | no | End date for DSCO change-log filtering. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scrollId` | string | no | Scroll identifier for DSCO change-log pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logs": [
        {}
      ],
      "scrollId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logs` | array<object> | Catalog change log records. |
| `scrollId` | string | Scroll ID for additional result pages. |

## Native endpoint

Through the native Rithum DSCO API, this operation is `GET catalog/log` (base URL `https://api.dsco.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog-change-log.md) for the provider-specific parameters and requirements.

