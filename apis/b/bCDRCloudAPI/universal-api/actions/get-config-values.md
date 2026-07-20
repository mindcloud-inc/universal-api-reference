# BCDR Cloud: Get Config Values



```
GET https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-config-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BCDR Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-config-values?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-config-values?${params}`, {
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
      "AG_DATE_FORMAT": "string",
      "AWS_OS_SUPPORT": 1,
      "ENABLE_NEWDASHBOARD": 1,
      "SG_CLIENT_IMG": "string",
      "SG_COMPANY_IMG": "string",
      "SG_PRD": "string",
      "SG_VERSION": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AG_DATE_FORMAT` | string | Configured date display format. |
| `AWS_OS_SUPPORT` | number | Whether AWS OS support is enabled. |
| `ENABLE_NEWDASHBOARD` | number | Whether the new dashboard is enabled. |
| `SG_CLIENT_IMG` | string | Filename for the client image asset. |
| `SG_COMPANY_IMG` | string | Filename for the company logo asset. |
| `SG_PRD` | string | Short product code. |
| `SG_VERSION` | string | Reported product version. |

## Native endpoint

Through the native BCDR Cloud API, this operation is `POST /getconfigvalue` (base URL `https://console1.bdrshield.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-config-values.md) for the provider-specific parameters and requirements.

