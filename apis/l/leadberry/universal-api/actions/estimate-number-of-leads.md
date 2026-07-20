# Leadberry: Estimate Number Of Leads



```
GET https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/estimate-number-of-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadberry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/estimate-number-of-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/estimate-number-of-leads?${params}`, {
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
| `aid` | string | no |  |
| `leadScoreLevel` | string | no |  |
| `pid` | string | no |  |
| `showBank` | string | no |  |
| `showGov` | string | no |  |
| `showHospital` | string | no |  |
| `showHotel` | string | no |  |
| `showSchools` | string | no |  |
| `wid` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadberry API returns.

## Native endpoint

Through the native Leadberry API, this operation is `GET /data/estimateNumberOfLeads` (base URL `https://app.leadberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-number-of-leads.md) for the provider-specific parameters and requirements.

