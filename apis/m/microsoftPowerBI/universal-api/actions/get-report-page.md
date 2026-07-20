# Microsoft Power BI: Get Report Page



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-report-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-report-page?connectionId=$CONNECTION_ID&groupId=string&reportId=string&pageName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string",
  "reportId": "string",
  "pageName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-report-page?${params}`, {
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
| `reportId` | string | yes | The report ID. |
| `pageName` | string | yes | The report page name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "name": "Ava Chen",
      "order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | The display name of the page. |
| `name` | string | The page name. |
| `order` | number | The display order of the page. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]/reports/[:reportId]/pages/[:pageName]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report-page.md) for the provider-specific parameters and requirements.

