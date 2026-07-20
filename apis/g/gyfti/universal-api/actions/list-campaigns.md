# gyfti: List Campaigns

Retrieves campaigns from gyfti.

```
GET https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gyfti `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/list-campaigns?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `constraints` | string | no | Optional URL-safe JSON array of Bubble search constraints, such as [{"key":"Campaign Type","constraint_type":"equals","value":"Trigger"}]. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Campaign Active Status": "string",
      "Campaign Status": "string",
      "Campaign Type": "string",
      "Campaign_Name": "Ava Chen",
      "Company owner": "string",
      "Cost": 1,
      "id": "string",
      "Owner": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Campaign Active Status` | string |  |
| `Campaign Status` | string |  |
| `Campaign Type` | string |  |
| `Campaign_Name` | string |  |
| `Company owner` | string |  |
| `Cost` | number |  |
| `id` | string |  |
| `Owner` | string |  |

## Native endpoint

Through the native gyfti API, this operation is `GET /obj/Campaign` (base URL `https://app.gyfti.fr/api/1.1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

