# Campaign Refinery: Get Forms

Retrieves all forms from Campaign Refinery.

```
GET https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Refinery `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-forms?${params}`, {
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
      "campaign_id": 1,
      "form_created_dts": "2026-05-07T12:00:00.000Z",
      "form_id": 1,
      "form_name": "Ava Chen",
      "form_uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_id` | number | Associated campaign ID when present. |
| `form_created_dts` | date | Form creation timestamp. |
| `form_id` | number | Campaign Refinery numeric form ID. |
| `form_name` | string | Form name. |
| `form_uuid` | string | Campaign Refinery form UUID. |

## Native endpoint

Through the native Campaign Refinery API, this operation is `GET /forms/get-forms` (base URL `https://app.campaignrefinery.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-forms.md) for the provider-specific parameters and requirements.

